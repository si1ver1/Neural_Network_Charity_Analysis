
# # Neural_Network_Charity_Analysis

## Overview
The goal of this project was to us a neural network to predict whether applicants given funding will succeed or not.

## Results
### Data Preprocessing
The variable considered the target for our model is 'IS_SUCCESSFUL' to determine whether or not the funding was useful 

The variables considered the features of the model are all of the remaining variable excluding the removed variables

The removed variables are 'EIN' and 'NAME'

### Compiling, Training, and Evaluating the Model
I ended up going with 3 layers with the neurons listed below. I went with this using the following formula
```
Where n = random number between 2-10
Neurons = (total samples) / (n * (number_of_inputs + 1))
Neurons = (34000) / (4 * (41))
Neurons = ~200
```
I then adjusted it slightly lower to use these values
```
hidden_nodes_layer1 =  120
hidden_nodes_layer2 = 30
hidden_nodes_layer3 = 12
```

I was unfortunately not able to achieve the >75% accuracy however I did improve the percentage by a small amount by changing the following:
- Reducing the unique values on some columns less than previously
- Increasing from 2 to 3 hidden layers
- Increasing the neurons used
- Changing the output activation to tanh
- I also tried removing some data from different areas such as the 5 rows is the status column with 0 but in the end all of these reduced the accuracy most likely because I was reducing the amount of data.

## Summary
Overall the accuracy of 72% is pretty decent but ideally we would achieve a higher amount for this. We could try running a different model such as a logistic regression model as we are trying to group our data into two sets.