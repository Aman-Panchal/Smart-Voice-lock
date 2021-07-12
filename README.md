# Smart-Voice-lock
Model to recognize the voive of user.
As we know speech is the most natural way of communicating for human beings. As digital signal processing technology advancement, speech has been used in many different  areas of application such as compression of speech enhancement, synthesis and  recognition. So in this we use voice for lock and unlock. 

In this firstly we created a dataset of audio of two person.We use librosa library to handle audio data set. And then use pydiogment for audio augmentation by various features such as adding noise shifting time changing speed and random cropping. And then use mfcc which iterate with every audio file and extract features from it. And than load this dataset through various classifier ml algos such as SGDClassifier, SVM, RandomForest and in last to deep neural network. Technology and tools wise this project covers:

    Python
    Librosa to handle audio dataset
    Matplotlib for data visualization
    Pydiogment for augmentation
    Sklearn for model building
    Speech recognition to covert audio to txt
    Jupyter notebook, Anaconda as IDE
