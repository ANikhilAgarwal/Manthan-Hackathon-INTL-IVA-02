#  📎 Manthan-Hackathon INTL-IVA-02
##  🎯 Face Recognition Through Varying Angles
#### Face Recognition based One Shot Learning, Siamese Learning
### Describe Your Approach towards Solution
We are undertaking a deep learning approach for building our face recognition model based on One Shot learning implemented through Siamese Network. The model will identify images if present in the input provided (image/video/live CCTV). Following the identification, the model is expected to recognize a suspect with an accuracy of more than 85% and send an alert to the concerned authorities if a match is confirmed.

For face detection, we are using Media Pipe Face Detection API, a machine learning framework developed in Python.
One-Shot learning, as specified above, is being implemented through Siamese Network, developed by using Python frameworks, namely, OpenCV, PyTorch/Tensorflow.

### Describe your idea in Detail no special Characters
Our idea deploys the concept of OneShot learning to identify a class of suspects by using one example of a class in this case a suspect implemented through the Siamese Network The network reduces the dimensionality of the images without losing valuable properties of the class example and compares the similarity scores of the input images with the ones present in the database 
Based on a preset threshold value the model returns a match for a given class and returns the so recognized identity on the web interface developed to implement our model The model further classifies each class as Known Unknown and Suspect Every time a class labeled Suspect is recognized the model sends out a popup alert to make the concerned authorities aware of the movement of the suspect

Our solution will be able to perform the following activities

 Detect the presence of multiple faces in an image or a video frame 
 Perform automatic feature extraction and metricbased learning 
 Identify new faces and recognize previously encountered identities
 Recognize an already identified individuals flagged as a suspects
 Alert authorities of the presence of the suspects in a given region 
 Share the profiles of recognized suspects including information such as Name Age Gender Timestamp and Related Video or Image Matched 
 Automatically learn and update metrics in the model from new input identities

 
Following is a brief description of how our solution will be developed and implemented on a live CCTV Feed

Our solution will gain access to the live CCTV feed by establishing connection through RealTime Streaming Protocol RTSP Having gained access to the live feed video frames will be fetched through OpenCV and fed into the Media Pipe Face Detection API for detecting faces Media Pipe will output image vectors having preprocessed tightly cropped faces These image vectors will act as input to the Siamese Network for feature extraction The model learns the metrics through One Shot Learning Pathak 2020 A feature map will be generated as an output of the neural network and crossreferenced with existing maps in the dataset to find matches Following this classification of identities will be undertaken into either of the following

Unknown
Known
Suspect

If the face is identified as unknown the model will label it and return the facial features extracted by the DNN If a match is found for the face the face is classified as known and a profile of the recognized face will be displayed on the page a template of the same is added in the next slide In case the identity match is recognized as a suspect an alert will be popped for the concerned law enforcement authorities 


 Considering computational compatibility issues we have kept ourselves open to implement Siamese network with either PyTorch or Keras Tensorflow 
 Considering deployment compatibility issues we have kept ourselves open to developing the webapp using Django or Flask

NOTE Several python libraries such as Numpy Pandas Sklearn etc will be used for complete development of our solution However we have only listed the ones used for building the spine of our solution 
