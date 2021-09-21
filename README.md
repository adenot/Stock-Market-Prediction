# Stock Market Prediction using LSTM (Research)
The main aim of this project is to increase the accuracy of the prediction model by tweaking several **hyper-parameters**. The number of **LSTM** layers used would be fixed (75 units) but the parameters that are being changed are:- **BATCH_SIZE** for LSTM, **EPOCHS** and previous **DAYS**.

## Abstract
**LSTM** or **Long Short-Term Memory** is an improvement over traditional **RNN** or **Recurrent Neural Network** in the sense that it can effectively “remember” **long sequence of events in the past**. Just like humans can derive information from the previous context and can chart his future actions, **RNN** and **LSTM** tends to imitate the same. The difference between **RNN** and **LSTM** is that **RNN** is used in places where the **retention of memory is short**, whereas **LSTM** is capable of connecting events that happened way earlier and the events that followed them.   
   
Hence, it (LSTM) is one of the **best** choices when it comes to analyzing and predicting **temporal dependent** phenomena which spans over a **long period** of time or multiple instances in the past.   
   
**LSTM** is capable of performing three main operations: **Forget**, **Input** and **Output**. These operations are made possible with the help of trained neural network layers like the **tanh layer** and the **sigmoid layer**. These layers decide whether an information needs to be **forgotten**, **updated** and what values need to be given as **output**. **LSTM** learns which parameter to learn, what to forget and what to be updated during the **training process**. That is the reason why **LSTM** requires a **huge amount of dataset** during its training and validation process for a **better result**. The **sigmoid layer** decides the flow of information. Whether it needs to allow all of the information or some of it or nothing.   
There are multiple gates that performs the role of **Forget**, **Input** and **Output**. These gates perform the respective operation on the **cell state** which carries information from the past. The **forget gate layer** tells the **LSTM** cell whether to keep the past information or completely throw away. The **input gate** determines what new information should be added to the cell state. The **output gate** finally gives the output which is a filtered version of the cell state.

## Background Information
### What is Machine Learning?
Machine learning is a branch of **artificial intelligence (AI)** and **computer science** which focuses on the use of data and algorithms to imitate the way that humans learn, gradually **improving its accuracy**.
### How is it Different from Deep Learning?
- **Machine Learning** is the superset. **Deep Learning** is the subset.
- ML is the ability of computers to learn and act with less human intervention.
- DL is all about mimicking the thinking capability of the human brain and arriving at a conclusion just like a human does after analyzing and thinking about it for a while.
### Artificial Intelligence vs Machine Learning vs Deep Learning   
![image](https://user-images.githubusercontent.com/55954313/133870891-0423a591-7518-45e7-8bfc-a125b82fa160.png)
### Neural Networks
**Neural networks**, also known as **Artificial Neural Networks (ANNs)** are a subset of **Machine Learning** and are at the **heart of Deep Learning algorithms**. Their name and structure are inspired by the human brain, mimicking the way that biological neurons signal to one another.   
   
It comprises of several **nodes** which represent **neurons**. A collection of nodes creates a **node layer**. These node layers play specific roles. Some acts as **input layer**, some **hidden layers** and some acts as **output layer**. Each **node**, or **artificial neuron**, connects to another and has an **associated weight and threshold**. It is by tweaking these weights and thresholds, that the network is able to learn progressively.   
   
There are different types of neural nets : **Convoluted Neural Networks**, **Recurrent Neural Networks**, etc.
### Simplest Neural Network
![image](https://user-images.githubusercontent.com/55954313/133871109-a721309a-9d14-435f-8d32-167c6b15c0d8.png)   
This is called a **perceptron**. It has only one **input layer**, one **hidden layer** comprising of only one **node** and one **output layer**.   
#### Source: https://www.ibm.com/in-en/cloud/learn/neural-networks
### Deep Neural Network
![image](https://user-images.githubusercontent.com/55954313/133872209-40ad4e68-71de-47d4-984d-499599da59f1.png)   
- Contains multiple hidden layers
- Since the depth of hidden layers is deep, hence the name.
#### Source: https://www.ibm.com/in-en/cloud/learn/neural-networks
### Recurrent Nueral Network
![image](https://user-images.githubusercontent.com/55954313/133872292-e603b584-8ad2-43d1-8bdf-863d66e4c823.png)   
#### Source: https://colah.github.io/posts/2015-08-Understanding-LSTMs
- Uses sequential data or time series
- Used in solving temporal dependent problems: Natural language processing, image captioning, speech recognition, voice search, translation, etc.
- Inefficient when it comes to prediction where the outcome is long term temporal dependent.
- The reason being Exploding and Vanishing gradient.
- LSTM overcomes the drawback
### Long Short Term Memory
![image](https://user-images.githubusercontent.com/55954313/134108241-e04cf3cb-e1ef-4aa0-b594-e147ea11d5cb.png)
#### Source: https://colah.github.io/posts/2015-08-Understanding-LSTMs
- Contains a cell state that carries information from one state to another
- Gates manipulate the info in the cell state. Three main gates used to do this are: **Forget gate**, **Input gate**, **Output gate**.   
   
![image](https://user-images.githubusercontent.com/55954313/134108503-8be7d9d1-ddd3-4dc9-863b-09d48d60162f.png)
- **Forget Gate**: Responsible for removing useless information. 
- **Input Gate**: Responsible for adding new information.
- **Output Gate**: Responsible for filtering out the information.

