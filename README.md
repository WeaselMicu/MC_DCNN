# MC_DCNN
## Multi channel deep convolutional neural network for time series classification.

MC-DCNN (http://staff.ustc.edu.cn/~cheneh/paper_pdf/2014/Yi-Zheng-WAIM2014.pdf) architecture, implemented with lasagne/theano. 

With the MC-DCNN architecture, features are first learned idependently on each channel with a
cascade of 1D convolutions and maxpooling, then the learned features are concatenated and fed into a MLP. 
The MLP is in charge of learning the correlations between channels and classification.

Here we train the MC-DCNN on a dataset of biometric data (ppg + accelerometer data time series), recorded over one month for 10 users. The MC-DCNN is trained to recoginze user ID based on its biometric data.
We achieve a classification F1 score of 0.97+.

This is a big improvement over a single channel DCNN implementation (F1 score ~0.85), where convolutions are performed over all channel simulatneously. 
