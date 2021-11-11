
# Smart-Voice-lock

Major Project of final year

•	Objective: Created an Arduino-based system of Smart-Voice Lock with the model of speech recognition using mfcc extraction. Which will increase security by using user voice to lock/unlock the system.

•	Used 200 audio files of two different people, then we use librosa library to handle audio files then perform data augmentation using pydiogment (which increases dataset to 600 audio files) by adding noise, shifting time and tone, random cropping and adjusting speed.

•	Use mfcc to extract features from audio files and then apply ML algos (SGDClassifier, Support Vector Machine, Random Forest Classifier) and DL algos in which Deep Learning outperforms well with an accuracy of 97.99%.

•	Also use google speech recognition library which converts the audio file into text to use as a command, if it matches the user's voice. 

![image](https://user-images.githubusercontent.com/62400307/125265558-94d03b80-e322-11eb-93f1-aaa53414d0c9.png)


## Why this project?
-Makes user experience easier.

-Increases security level.

-Useful for disabled person.

## Introduction
The Objective of  Project:-
The objective of the project is design an IOT based system of smart voice lock with the model of speech recognition using MFCC extraction. This device lock/unlock on user voice.

Description Of the Solution Implemented:-

The motivation for smart voice lock with speech recognition is simple; It is main principle of communication and is, therefore, a convenient and accessible way of communication with machines.
And we can easily use this technology  to interact with various electronic devices . And in our project we used it to lock and unlock the lockage’s. We can use use user voice and perform speech processing by using various machine learning and neural networks and train a model which match the voice of user and if get match than he can operate the device/lock . 


## Approach to solve problem 
1. Frame the problem
2. Get the Data
3. Explore the data to gain insight
4. Prepare the data for Machine Learning  algorithms 
5. Explore many different models and short list best one
6. Fine Tune the model
7. Present solution

## Install dependecies
pydiogment 
```
!pip install pydiogment
!pip install -U pydiogment
```
librosa
```
!pip install librosa
```
speech_recognition
```
pip install speech_recognition
```

## Data
The audio dataset is a small dataset consist of 200 audio files of English sentences of 25 lines with 4 repetition of each line for each of two different speakers. Audio average .5 seconds of length. Each of this audio is labeled with two labels person1 and person2. And the dataset is labeled so we can easily perform supervised machine learning algorithms.

Than created augmentation to upscale the dataset. Than use mfcc library. And by using this library we convert these audio files into numerical values and extract features.
![image](https://miro.medium.com/max/996/1*H_lcPB14mWwXrbN_ibIeGw.jpeg)
Then divide this into two for training and testing into 80:20 ratios. Training part is used for different machine learning algorithm.

| Features |class |
| :-------- |:-------- |
| [-371.93112, 145.489, -22.60909, 18.450535, 40...|aman|
| [-430.44672, 200.24297, -58.688416, 23.587633,...|aman|
| [-415.59647, 154.93677, -23.800282, 16.818874,... |akash|
| [-406.82013, 154.63939, -25.195005, 15.650413,.. |akash|


## Result

|    |**Model** | **Training Accuracy %**    | **Testing Accuracy %**             |
| :- | :-------- | :------- | :------------------------- |
| 1| `SGDClassifier` | 94.43 |   95.17|
| 2|`Support Vector Machine` |  100.00 |  71.38 |
| 3|`Random Forest Classifier` |  	97.66 |  97.42 |

**Deep Neural Network**

Activation = Relu and Softmax

Dropout = 0.5

loss ='categorical_crossentropy'

optimizer ='adam'
   
accuracy : 97.99%

## Future Scope
~ Connect it with cloud based server and create database of user.

~ It works on multiple voices at same time.

~ Make it more secure by innovating new features of sound.

## Future Scope
**Library**:

 Audio Augmentation- https://pythonawesome.com/python-library-for-audio-augmentation/


**Research Paper**:
 1. https://paperswithcode.com/task/audio-classification
 2. https://duckduckgo.com/?q=human+voice+dataset&t=newext&atb=v247-1&ia=images
 3. https://link.springer.com/chapter/10.1007/978-3-319-13102-3_72
 4. https://www.hindawi.com/journals/wcmc/2020/6138637/
 5. https://www.scirp.org/Journal/PaperInformation.aspx?PaperID=88650



