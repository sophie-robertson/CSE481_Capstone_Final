# CSE481_Capstone

First look at necapstone_env.yml to create a conda environment and install dependencies!\
    Run `conda env create --name <name> --file=necapstone_env.yml`

Muscles: contains images of different upper body muscles affected by our model\
\
Model: Contains code for our RNN model, training, and hyperparameter tuning. In addition there are files specifically for use with CUDA. Please look at the mrnn.py and training.ipynb\
\
    training.ipynb is our training and testing file - it shows how the model is used\
    mrnn.py is our model implementation \
    top5_tuning are the pickle objects containing our model predictions for the top 5 hyper parameter configurations as determined by our grid search \
    \
GUI: Contains files for our GUI. To open the GUI, please run gui.ipynb. Look at metrics.py to see how the metrics were calculated 
\
\
\
Data:

The data is stored in `monkey_data.mat`. It holds 1 session of trials, which is 502 trials. For each trial, there is data for `['inp']` and `['targ']` representing the input and true output respectively. \
\
The input data is 21xtrial_length. The first 20 dimensions are the 20 first principle components from an image of the grasping target. The 21st dimension is the hold signal, which is 1 when the network should not output muscle movement, and 0 when it should. \
\
The output data is 50xtrial_length. Each of the 50 dimensions refers to a different muscle's velocity. The code for the data loading is in the file `mrnn.py`. 
