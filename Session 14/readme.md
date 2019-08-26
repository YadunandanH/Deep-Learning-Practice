# Assignment 14

Our team tried multiple approches to increase the accuracy of the model.

### Approch 1:
1) We tried reducing number of parameters by using c=32.
2) Used 3 residual blocks instead of 2
3) Used 1 cycle LR policy
4) Used model concatination 
5) Used cutout 
using this approch acheived validation accuracy of 93.2% 
Time taken: 850 seconds in colab

### Approach 2:
Used the same network as of Approch 1 along with that tried sceduling the Momentum as mentioned by Leslie Smith.
But after using this approach validation accuracy decreased.

### Approach 3:
1) Used the default architecture provided
2) Added 1 extra residual block
3) Used 1 cyle LR(0.4) 
4) Image augumentaions used: zoom_range=0.0,rotation_range=30 ,featurewise_center=True,featurewise_std_normalization=True,                             horizontal_flip=True,cutout
5) Used tfrecord implementations
Approach 3 is giving us 95.2% validation accuracy on v100 GPU(Floyd)
time taken: 29 Seconds

Note: In notebook final log avoided printing training loss and training accuracy, only we can see validation loss and validation accuray

