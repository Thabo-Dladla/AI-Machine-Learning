# Assignment 4: Neural Networks  
# Assignment goal: Optimisation of a Neural Network for Image Classification  
# Dataset-> Fashion-MNIST dataset
# classes/labels of the dataset -> T-shirt/top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle boot.

# DEPENCIES :   
**pandas**  
**Numpy**  
**Pytorch**  
**Scikit-learn**  
**matplotlib**  
**random**  

# OVER-VIEW  
**To build a neural network, implement the data processing and training process**  
**including backpropagation, and experimentally discover how hyper-parameters impact performance**    
**The hyper-parameters I choose to experimentally vary are-> Learning rate ,Optimizers and The number of neurons in hidden layer one**  


# setup instructions
# The notebook works with the CSV format/version of the FASHION-MNIST dataset  
**DATA should be in the following format**  
**kaggle/fashion-mnist_train.csv - training dataset**   
**kaggle/fashion-mnist_test.csv - test dataset (used as validation set for this assignment)**   

# Report.pdf  
**File containing my motivations for the choices I made and my findings and while experimenting**  

# In My main fle the notebook -> Assignment4.ipynb
# 1. Data processing  
**Loading in the data and processing it**  

# 2. Building and training a Baseline model  
**Here we build a baseline model that we will compare against when trying different hyperparameter settings later**  
**We build a simple, standard neural network and train it for 10 epochs with default settings**  

# Baseline Model Architecture:  
**->A simple Multi-Layer Perceptron (MLP) with the following architecture:**  
**○ Input Layer (a flattening layer).**  
**○ Hidden Layer 1: 128 neurons, ReLU activation.**  
**○ Hidden Layer 2: 64 neurons, ReLU activation.**  
**○ Output Layer: 10 neurons (one for each class).** 

**The default settings are:** 
**"torch.optim.Adam with a default learning rate of 0.001"**  
**The baseline model will train for 10 epochs and then we record its final accuracy on the validation set: This will be the baseline accuracy**  

# 3. Hyperparameter Optimisation Experiment  
**Chosen Hyperparameters :**  
**->learning_rates = 0.1, 0.01, 0.001**  
**->optimizers = 'Adam', 'SGD', 'RMSprop'**  
**->Number of neurons in the hidden layer one = 64, 128, 256**  

**We then train all 36 combinations and take the one with highest validation accuarcy as the best overall model**  
**Hyperparameter experiments all use the same neural network "NeuralNet" class as the baseline model**  
**And the also use the same training loop , training for 10 epochs**  
**this is to make ti fair to compare any model attained from experimenting because it would have gone through the same training and validation process**    
**and then for each combination/model we then record the final accuracy on the validation set**  
**The Best Combination I attained:**  
**Learning rate: 0.0005**  
**Optimizer: RMSprop**  
**Hidden layer one Neurons: 512**  
**Accuracy: 89.84%**  

# 4. Part 4: Analysis and Report  
**Bar chrats visualizing the impact of each hyperparameter :**  
**These shows the average validation accuarcy by each hyperparameter**  

**Best Model vs Baseline model :loss curves, to help to visualize overfitting and serve as evidence for my report for when I answer the question:**  
**"Did your hyperparameter tuning help mitigate overfitting?"**  

**A confusion matrix: for my best model's predictions on the validation set, this helps to see which clothing items are being confused**  

 
