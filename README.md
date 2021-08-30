# Neural Network Charity Analysis

## **Overview of the Analysis**
Th purpose of this analysis is to help the non-profit foundation, Alphabet Soup, by analyzing the impact of each donation and vet the donation recipients using an optimized deep layer neural network model.  We want the model to predict with a 75% plus accuracy which organization recipients are likely to use the funds effectively and impactfully, so that Alphabet Soup can determine whether a donation will be worthy or too risky.

## Results

### _Data Preprocessing_

* The variable chosen as the target for my model was **"IS_SUCCESSFUL"**.

* The variables chosen as my features for my model were 'APPLICATION_TYPE', "AFFILIATION','CLASSIFICATION','USE_CASE','ORGANIZATION','INCOME_AMT', and 'SPECIAL_CONSIDERATIONS'.

* The variables that were neither targets or features, but were initially dropped from the original dataset, were 'EIN' and 'NAME'.
 
### _Compiling, Training and Evaluating the Model_

* For my initial model, I had 2 layers.  The first layer was initialized with 80 neurons and the second layer had 30 neurons.  The activation function for the first and second layers was "ReLu" and the output layer's activition function was "Sigmoid".  These were selected because the activation function ReLU is high functioning for non-linear data and the 80/30 neuron split between the layers was a good starting baseline. This model had 2 hidden layers for deep learning to train the model with a possible higher accuracy.
 
* The target model performance was set at 75% or greater. The original model maintained the highest accuracy score of 74.09%, which was just short of a 75% predictive accuracy.
  
**Original Model**

![image](https://user-images.githubusercontent.com/79073778/131261617-aaf71f60-1e39-44f0-ba68-524a1acf325e.png)


* I ran this model at least 8 times with changes to the dataset features or bucket bin measurement, the layers, the neurons, the activation functions and the epochs.  Listed are 5 Optimization steps taken to try to increase model performance:
 
### Optimization 1
Steps: Dropped columns (Affiliation, Classification, Special_Considerations); Node 1 = 100, Node 2 = 40; 1st & 2nd Layer = Tanh; 
Epochs = 130
![image](https://user-images.githubusercontent.com/79073778/131261714-d0fa659f-8205-4d06-bc64-15bc60b2d889.png)


### Optimization 2
Steps: Dropped columns (Affiliation, Classification, Special_Considerations); Node 1 = 100, Node 2 = 75; 1st & 2nd Layer = Linear; 
Epochs = 200
![image](https://user-images.githubusercontent.com/79073778/131261821-c3d7cbd1-0ceb-487e-8903-93ac744c6b52.png)


### Optimization 3
Steps: Dropped columns (Organization, Special_Considerations); Application bin < 700; Node 1 = 100, Node 2 = 45; 1st & 2nd Layer = ReLu; 
Epochs = 100
![image](https://user-images.githubusercontent.com/79073778/131261981-02fa8219-8992-4e79-87e6-066498df0d1f.png)


### Optimization 4
Steps: Dropped columns (Income_Amt, Special_Considerations); Application bin < 500; Node 1 = 30, Node 2 = 80; 1st & 2nd Layer = ReLu; 
Epochs = 125
![image](https://user-images.githubusercontent.com/79073778/131261993-374b72b8-7b72-4947-bdb5-9c130ec4235c.png)


### Optimization 5
Steps: Dropped columns (Income_Amt); Application bin < 500; Node 1 = 60, Node 2 = 20; 1st & 2nd Layer = ReLu; Epochs = 100
![image](https://user-images.githubusercontent.com/79073778/131262039-80f535a9-3c76-4c78-8530-0b6d30c74e47.png)


## Summary

My 5 attempts at optimizing the deep learning model stayed pretty consistent at 73% for the loss and predictive accuracy.  But, none of the 4 optimizing attempts ever exceeded the original analysis accuracy outcome of 74% or hit the predictive accuracy target of 75%.  I actually tried two attempts with 3 layers using leaky ReLu and linear activation functions in the 2nd and 3rd layers, but the loss and predictive accuracy was far worse with a loss of 58% and predictive accuracy of about 63% compared to the deep learning model with only two layers.  
I attempted to run the model using the Random Forest Classifier. The outcome was the same for a predictive accuracy of 73.52% even trying it with different activation functions. This model using Random Forest Classifier did not meet the predictive requirement, either.  
Therefore, I would **recommend** to use the original model as the predictive accuracy was closer to 75% than all the other model optimization attempts.
