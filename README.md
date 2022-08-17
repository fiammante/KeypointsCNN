# KeypointsCNN
A Jupyter Notebook that shows the merge of classical Keypoints Detector (ORB) result to a categorization CNN
https://docs.opencv.org/3.4/d1/d89/tutorial_py_orb.html
Key points algorithms detect points that are repeatable and distinctive at multi scale and rotation of image.

The approach is to use ORB to create masks on the training and test datasets, Fashion_Mnist in this example, 
create training and test images that either only contain keypoints or only non keypoint areas and train a one convolution layer discriminator.
The trained layer weights are then used as the first categorization CNN convolution layer weights.

The results are after 50 epochs
Without discriminator weights
Test loss: 0.4718182682991028
Test accuracy: 0.9043999910354614

With discriminator weights and further training of that layer 
Test loss: 0.47225576639175415
Test accuracy: 0.9150999784469604

With discriminator weights and frozen training of that layer 
Test loss: 0.48668134212493896
Test accuracy: 0.9110999703407288
