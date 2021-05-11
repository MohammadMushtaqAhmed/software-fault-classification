# Software Fault-Prone Module Classification Using Learning Automata based Deep Neural Networks
Defects are common in software systems. But they will show adverse effects on the use of the application. Sometimes these defects will lead to software failures. Using software fault-prone classification models will reduce software failures. And more companies have to spend most of the budget in the testing phase only. So, software engineers should check the module which has a defect to reduce the cost. This model leverages deep learning techniques to classify the modules into faulty and non-faulty modules using learning automata.

An overview of the learning automata-based deep learning model is shown in below figure. The proposed approach is divided into two phases: training the learning automata-based deep learning model (i.e.,LADNN model) and classifying the new software modules into fault-prone modules based on the trained model. To classify a software module into fault-prone module, we perform the following key steps.
- First, we collect datasets containing software metrics.
- Second, we perform data preprocessing techniques (data log transformation and data min-max normalization) on the given software metrics.
- Third, in the training phase, we train a specially designed learning automata-based deep learning model to classify a software module as fault-prone or not fault-prone.
- Finally, in the testing phase, we perform the data preprocessing techniques on new software module metrics and then this preprocessed data is as input to the trained model to classify the software module as faultproneor not fault-prone.
![model_diagram](https://user-images.githubusercontent.com/83901192/117777727-85693f00-b25a-11eb-9921-339ab5399ed6.png)

## Learning Automata based Deep Neural Network model

We propose a learning automata based deep learning neural network (LADNN) model for software fault-prone classification. An overview of the fully connected
network is shown in below figure. We preprocess the software metrics and input them to the model. The model classifies each module into fault-prone
or not fault-prone. We set the input dimensions, output dimensions and activation function for each layer as follows:

First layer: input_dim = 22, output_dim = 20 and activation function =‘Relu’.

Second layer: output_dim = 10 and activation function = ‘Relu’.

Output layer: output_dim = 2 and activation function = ‘Softmax’.

![SDP](https://user-images.githubusercontent.com/83901192/117778902-c2820100-b25b-11eb-8179-a9e10e12e229.png)


## Parameters meaning in code:
- `eta`: learning rate
- `max_epochs`: maximum number of iterations
- `la_size`: number of neural units in each LCU
- `global_delta`: step size for LA probability updates

## Code Execution Steps:
1. Modify the parameters, which are globally declared as per the requirements.
1. To modify the neural network model, change the number of neurons array and activation
functions array in the main and do the same in cross validation function.
1. To run the code on a dataset, upload the dataset and then read the dataset by writing its
name in get_data function.
