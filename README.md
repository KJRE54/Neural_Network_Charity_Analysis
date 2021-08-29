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

![image](https://user-images.githubusercontent.com/79073778/131237079-ba9c6e76-870e-4286-bafb-2f3f8e41ebc8.png)

* I ran this model at least 6 times with changes to the dataset features or bucket bin measurement, the layers, the neurons, the activation functions and the epochs.  Listed are 3 Optimization steps taken to increase model performance:
 
**Optimization 1**

![image](https://user-images.githubusercontent.com/79073778/131237258-ad829a5c-2045-4f8d-a9c5-5a8e7dc23d92.png)


### Optimization  2



### Optimization 3
