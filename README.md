# Overview of the analysis: 

The goal of this analysis is to build a binary classification model using a neural network that predicts whether an organization will be successful in using the funding it receives from the Alphabet Soup nonprofit foundation. The outcome will help Alphabet Soup decide which funding applicants are most likely to succeed.

# Results: 


## Data Preprocessing
- What variable(s) are the target(s) for your model?
    - IS_SUCCESSFUL — This column indicates whether the organization successfully used the funds and is the binary target variable (1 = successful, 0 = not successful).
- What variable(s) are the features for your model?
    - All columns except IS_SUCCESSFUL, EIN, and NAME were used as features.
- What variable(s) should be removed from the input data because they are neither targets nor features?
    - EIN and NAME — These were identification fields with no predictive power and were dropped before training.

## Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - Initial Model (AlphabetSoupCharity.ipynb):
        - 1st layer: 8 neurons, relu activation
        - 2nd layer: 5 neurons, relu activation
        - Output layer: 1 neuron, sigmoid activation
    - Optimized Model (AlphabetSoupCharity_Optimization.ipynb):
        - 1st layer: 32 neurons, relu
        - 2nd layer: 16 neurons, relu
        - 3rd layer: 8 neurons, relu
        - Output layer: 1 neuron, sigmoid
- Were you able to achieve the target model performance?
    - I was not able to get to at least 75% accuracy after multiple optimization attempts. 
- What steps did you take in your attempts to increase model performance?
    - Optimized model architecture: added more layers and neurons.
    - Feature engineering: removed low-frequency categorical levels, encoded categorical variables.
    - Data standardization: used StandardScaler for scaling numerical features.
    - Introduced validation_split during training to evaluate model generalization.

# Summary: 
### Overall Results:
- A deep learning model was built and optimized to classify funding success based on organizational data.
- Optimization included restructuring the neural network with additional layers and more neurons to improve performance.
- Accuracy improved with the enhanced architecture, although exact metrics would confirm the extent of improvement.
   
### Recommendation:
Try experimenting with other models such as Random Forest Classifier. Tree-based models handle categorical variables well, are robust to outliers, and can provide feature importance for better business insights.
