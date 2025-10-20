# CSC2042S 2025  
# Assignment 3  
# Logistic Regression: for English and IsiXhosa  

# DEPENCIES :  
**pandas**  
**Numpy**  
**Pytorch**  
**Scikit-learn**  
**matplotlib**  
**re**   
**random**  

# OVER-VIEW   
**To train and evaluate separate models for two languages: English and**  
**isiXhosa. Each language covers a different subset of news categories, so the number of classes**  
**will not be constant. They also differ linguistically and in the size/quality of their datasets, which**  
**may affect the difficulty of the classification task and the role of feature extraction.**  
**The aim is to experiment with hyperparameters and modelling decisions to analyse how they**  
**affect performance for each language**  

# setup instructions  
**DATA should be in the following formatt**  
**A3-dataset/eng/- English dataset (train.tsv, dev.tsv, test.tsv, labels.txt)**   
**A3-dataset/xho/- isiXhosa dataset (train.tsv, dev.tsv, test.tsv, labels.txt)**   

# Report.pdf  
**File containing my motivations for the choices I made and my finding and while experimenting**  

# 1. Data processing  
**Created a cunctom made text cleaner to allow for varuing cleaning methods such as cleaning emails if the prove to not be important**  
**I implemented a way to remove the stop word for isiXhosa**  
**To test if it would improve performance and to check how it affects the size of the vocabulary for the different feature extraction methods**  

# 2. Multinomial logistic regression implementation   
**Implemented the Multinomial logistic regression using pytorch**  
**● forward: process a batch of inputs during training.**  
**● compute_probabilities: compute probabilities for a batch of inputs.**  
**● predict: return the predicted classes for a batch of inputs.**  
**●get_weights: returning the weights learnt for later analysis**  

# 3. Training  
**Trying different stopping conditions with the aim of minimizing overfitting for both models**  
**
# 4. Hyperparameter tuning & 5. Feature extraction  
**Tuning hyperparameters such as batch size for cross-entropy loss,learning rate and Vocabulary size**  
**To find the best configuration for each language and feature extraction method**
**Feature extraction methods include:**  
**●Bag Of Words**
**●Binary**  
**●FTIDF**  
**IsiXhosa excelled when using Binary getting a validation accuracy 92,52%**  
**while English excelled when using TFIDF ,getting a validation accuracy of 89.83%**   

# 6. isiXhosa training decisions-Dues to isiXhosa having imbalanced datasets  
**Applying L2 and L1 Regularizations to the best isiXhosa model to see if they can each improve performance**   
**Also applied upsampling and down sampling to address imbalance of classes within the isiXhosa datasets**  
**The aim was to vary the coefficients for Regularizations and to separately vary the sampling rates for when addressing  class imbalance**    

# 7. Evaluation    
**Evaluating my best Models for each language ,for English I had one and for isiXhosa I had two, the 2nd one attained from the regularization/ Handling class imbalance experiments**  
**These models were evaluted on the test set upon which they shall be analysed for their respective macro and micro averages for f1-scores , presicion and recall**  


# 8. Weight analysis  
**For any of the languuages the aim was to analyse the learned softmax weights**  
**And to the identify whether specific keywords or groups of words strongly contribute to certain categories.**  
**And to give examples where the model has learned plausible associations, or cases where it may be overfitting**  
**or learning incorrect association**  

