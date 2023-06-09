# Neural Network Charity Analysis

## Overview
 - Creating a binary classifier neural network that is capable of predicting whether applicants will be successful if funded by the Alphabet Soup Charity.
### Deliverables 
 - Deliverable 1: Preprocessing Data for a Neural Network Model
 - Deliverable 2: Compile, Train, and Evaluate the Model
 - Deliverable 3: Optimize the Model
 - Deliverable 4: A Written Report on the Neural Network Model
-------------
## Results

### Data Preprocessing
 - Columns "EIN" and "NAME" were dropped as they were ID columns, and therefore not needed for the model.
 - Columns "APPLICATION_TYPE" and "CLASSIFICATION" were subjected to binning in order to reduce the number of unique values.
 - The categorical data is separated into a new data frame to be encoded using OneHotEncoder. After being encoded, the new data frame is merged back with the original dataset (while dropping the original non-encoded columns).
 - The data is split into both training and testing variables, then is scaled using StandardScaler.
### Compiling, Training, and Evaluation
 - This model used two hidden layers and an output layer. The first hidden layer had 80 neurons and used a ReLU function, while the second layer had 30 neurons and also used a ReLU function. For the output layer, the Sigmoid funtion was used as the activation function.
 - The model had an accuracy of 73%, a loss metric of 55.7%, and was unable achieve target model performance.
### Optimization
 - Attempt 1: More neurons were added to both of the hidden layers (140 (layer one) and 80 (layer two). The model accuracy was 72.8% and the loss metric was 56.5%
 - Attempt 2: An extra hidden layer was added. The third hidden layer had a total of 20 neurons (First and second hidden layers were also given extra nodes, 100 and 50 respectively). The model accuracy was 72.7% with a loss metric of 56.6%
 - Attempt 3: The activation function of the hidden layers was changed to tanh and the number of epochs was increased to 150. The model accuracy was 72.8% with a loss metric of 55.8%
 ----------
 ## Summary 
 - In conclusion, my neural network model failed to reach the accuracy of 75% or above. A recommendation that could be applied to help improve the model is using the Keras Tuner from TensorFlow, which helps pick the optimal set of hyperparameters for your model. Using this might help in getting the hyperparameters correctly optimized in such way that it boosts the accuracy.
