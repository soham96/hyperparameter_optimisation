# Hyperparameter Optimization

In this repo, we use two hyperparameter optimisation techniques: Grid Search and Bayesian Optimisation to train two Neural Network Architectures: Feed Forward Neural Network and Convolutional Neural Network on the MNIST dataset.

## Installation
`pip install -r requirements.txt`  
Run the above command to install the required packages

## Work Done

### Grid Search
Grid Search is a brute force approach to perform hyperparameter optimisation. It basically uses all the combinations of hyperparameters and gives the network with the highest output. This can be easily parallelised since each run is independent of other runs. A more advanced version of this is random search which randomly initialises the hyperparameters.

I have used the `hyperas` library which is a wrapper over the `hyperopt` library to perform grid search.

You can see the results in the `Grid_Search.ipynb` notebook.

### Bayesian Optimisation
Bayesian Optimisation is a more smart way to perform the hyperparameter search. Using the results of previously trained models, it can better adjust which hyperparameters to use next. This is why it is hard to perform parallely.

I have used `bayes_opt` package to perform bayesian hyperparameter optimisation using Gauusain Process. Using this, given the search space, I was able to find a set of hyperparameters that gave the highest testing accuracy on MNIST.

You can see the results in the `Bayesian_Optimisation.ipynb` notebook.

## Running the notebooks
You can run the notebooks in your local machine. However, given the large search space, it might take a long time to complete the training. Therefore it is better to run it on a powerful machine. I have google colab for this. You can find the notebooks here:
- [Grid Search](https://colab.research.google.com/drive/1iA6peiCnrFRS24r_H9uV1_nMeUVy2oXr)
- [Bayesian Optimsation](https://colab.research.google.com/drive/1VinHILP_TOx_MN1_bbC4fTKaq_xIAUv0)
