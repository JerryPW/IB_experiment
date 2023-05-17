# IB_experiment
## Description
This is the final project of Information Theory in SJTU, and the main topic of this project is Information Bottleneck Problem. The code here is just for validation. 

## Prerequisites
- tensorflow r1.0 or higher version
- numpy 1.11.0
- matplotlib 2.0.2
- multiprocessing
- joblib

## Usage
All the code is under the `idnns/` directory.
Set up the conda environment: 
```
conda env create -f environment.yml
conda activate IDNN
```
For training a network and calculate the MI and the gradients of it run the an example in [main.py](main.py).
```
python main.py
```
Off course you can also run only specific methods for running only the training procedure/calculating the MI.
This file has command-line arguments as follow - 
 - `start_samples` - The number of the first sample for calculate the information
 - `batch_size` - The size of the batch
 - `learning_rate` - The learning rate of the network
 - `num_repeat` - The number of times to run the network
 - `num_epochs` - maximum number of epochs for training
 - `net_arch` - The architecture of the networks
 - `per_data` - The percent of the training data
 - `name` - The name for saving the results
 - `data_name` - The dataset name
 - `num_samples` - The max number of indexes for calculate the information
 - `save_ws` - True if we want to save the outputs of the network
 - `calc_information` - 1 if we want to calculate the MI of the network
 - `save_grads` - True if we want to save the gradients of the network
 - `run_in_parallel` - True if we want to run all the networks in parallel mode
 - `num_of_bins` - The number of bins that we divide the neurons' output
 - `activation_function` - The activation function of the model 0 for thnh 1 for RelU'
 - `interval_accuracy_display` - The interval for display accuracy
 - `interval_information_display` - The interval for display the information calculation
 - `cov_net` - True if we want covnet
 - `rand_labels` - True if we want to set random labels
 - `data_dir` - The directory for finding the data
The results are save under the folder jobs. Each run create a directory with a name that contains the run properties. In this directory there are the data.pickle file with the data of run and python file that is a copy of the file that create this run.
The data is under the data directory. 

