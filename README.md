# CSE481_Capstone

First look at necapstone_env.yml to create a conda environment and install dependencies!\
    Run `conda env create --name <name of your choice> --file=necapstone_enc.yml`

Muscles: contains images of different upper body muscles affected by our model\
\
Model: Contains code for our RNN model, training, and hyperparameter tuning. In addition there are files specifically for use with CUDA. Please look at the mrnn.py and training.ipynb\
\
    training.ipynb is our training and testing file - it shows how the model is used\
    mrnn.py is our model implementation \
    top5_tuning are the pickle objects containing our model predictions for the top 5 hyper parameter configurations as determined by our grid search \
    \
GUI: Contains files for our GUI. To open the GUI, please run gui.ipynb. Look at metrics.py to see how the metrics were calculated 