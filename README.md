# Face-detection-and-recognition
## Libraries 
1.) OpenCv
2.) OS
3.) Numpy
## Project Description
I have created a very basic Facial recognition system using Cascade classifier and KNN for training and predicting the results.
First in my face_data_collect.py file i have collected data for the training purpose.I have converted each captured in
grayScale(converted to 1 channel) so that computation is reduced.I tried Gaussian blur at each frame but results were not
so efficient.The Value in detectMultiScale for minNeighbors is taken 5 and scale factor is 1.3(standard values).Faces
are sorted  based on the the area of faces of same frame.Then the data is appended in the list face_data for every
10th frame.Rectangle around the face detected in the captured frame is drawn in each iteration.Our dataset for the 
faces is stored in the numpy array format in the numpy python file(.npy extenstion) in the folder for each respective 
person face.

Then in the file face_recogition.py I have trained ,prepared as well as tested the data.Class id is mapped to respective
person by loading the respective .npy file.Labels are created to each class.Then for testing KNN predicts the class ie. 
name of the person in the current frame according to the face using K nearest neighbour approach by comparing training 
data to frame captured.
