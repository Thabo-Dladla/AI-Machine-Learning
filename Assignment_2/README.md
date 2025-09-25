# CSC2042S 2025 – Assignment 1: Milticlass-Perceptron for the Simpson images for GRAYSCALE images and RGB images

# Libraries used
**numpy,PIL,os,sklearn,random and matplotlib**  

# Excpected File Structure  

**Simpsons MNIST/**  
**├── grayscale/**  
**│   ├── train/**  
**│   │   ├── bart simpson/**  
**│   │   ├── charles montgomery burns/**  
**│   │   ├── ... (all 10 classes)**  
**│   └── test/**  
**│       ├── bart simpson/**  
**│       ├── ... (all 10 classes)**  
**└── rgb/**  
**    ├── train/**  
**    └── test/**  

# The report(Report.pdf)
**-A detailed report about my finding and comparisons between the two image types: RGB and Grayscale**  
**-The report is based on manual and automated testing e.g. testing for different stopping conditions so as to nah have any overfitting**  


# assignment2.ipynb(notebook)
# 1. Data processing  
**-Loading and flattening data and applying normalization:**  
**-Here we process the data and splitting the already given test set futher into both a new test set and a validation set**
**-The split follows an 80%  training and 20% validation rule and then we also define the normlization functions**  
**-Its important to note that the normalization parameters such as standard deviation and mean are opnly ever computed from the training set and then used in both the tst set and validation sets**  
**-Note: 'nomalization' is for the 0-1 normalization using the min and max of each feature/pixel in this case**  

# 2. Multi-class perceptron implementation  
**Binary class definition**  
**In the BinaryPerceptron class I treated bias as a weight as well following the linear algebra notaion where b = w0**  
**This is done to make it so that the bias terms undergoes the same initialisation as all the weights**  

# MulticlassPerceptron   
  
**0 to 1 normalization**  
**a learning rate of 0.01**  
**the intialisation strategy was kept as foolowing the uniform distrbution**  
**The training loop is defined within this class**  


# 3. Training  

# Trying different stopping condtions  for both the RGB and Grayscale  
**a)Fixed Number of Epochs**  
**b)Early Stopping with Different Patience**  

# 4. Hyperparameter tuning  
**here I trained using a maximum of 36 combinations of the following hyper-parameters**  
**learning rate, normalization strategy and intialization strategy**  

# 5. Evaluation  
**Here we run the best models for the RGB and Grayscale images againts the test set to do one final test on our model**  
**We then compare th two on a per class basis and overall basis :using accuracy and**  
**● Accuracy**  
**● Precision**  
**● Recall**  
**● F1**  