# deep_learning_challenge

The report should contain the following:

Overview of the analysis: Explain the purpose of this analysis.

The purpose of this analysis was to design and run a neural network model that can sucessfully predict whether a applicants will be sucessful in theor ventures; if they recieve the funding from Alaphabet Soup. 

Results: Using bulleted lists and images to support your answers, address the following questions:

Data Preprocessing

What variable(s) are the target(s) for your model?
The target variables for the model were the is_sucessful column. This showd in the training data set if previous clients that were selected, ended up being sucessful after recieving the funding. 

What variable(s) are the features for your model?
What variable(s) should be removed from the input data because they are neither targets nor features?

The rest of the variables in the dataframe are the features for training the model. I ended up only dropping the EIN column and using the NAME column, This was done so that I could have more variables to better train and compile the data. When using the NAME column, I was able to achieve an accuracy score of 79.5%. Without the NAME column, the highest I was able to achieve was a 72%. 

Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?

I chose to use 1000 neurons and had the input dimention set to the shpae of my X (features) data set. THe activation layer used a leaky RELU function so that it could filter the data but wasnt as harsh as a strictly RELU function. The second layer used half the neurons and a Sigmoid function. The final layer had 1 neuron and a Sigmoid finction as well. This is standar to use as an output layer. 

Were you able to achieve the target model performance?
I was able to achieve an accuracy scoure of almost 80% with 12 epochs. If I had more epochs, I predict the score could be a litte higher. 

What steps did you take in your attempts to increase model performance?
I first tried binning more buckets to reduce the number of potential outliers. That didnt have much sucess so I tried increasing the number of epochs. That also leveled out at aound 73%. Lastly I tried adding more columns by including the NAME column and binning it so that it only included names that were used multiple times. This helped achieve an accuracy score of 79.5%. 


