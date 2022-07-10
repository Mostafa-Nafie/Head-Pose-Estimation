# Head Pose Estimation
This project tries to find the direction a person is looking using the orientation of the head.  
Head orientation can be defined using pitch, yaw, and roll, so I used a machine learning model tries to estimate these values using facial landmarks.
<p align="center"> <img alt="head rotations" src="https://user-images.githubusercontent.com/44211916/177429857-0021ef17-c7bd-4584-874e-e3e8a5ccbf85.png"></p>

## Demo:
https://user-images.githubusercontent.com/44211916/178145301-f9dd0f51-3912-4ee6-a8da-9a9f4f3b674d.mp4



## Dataset:  
For this project, the dataset used is <a href=http://www.cbsr.ia.ac.cn/users/xiangyuzhu/projects/3DDFA/Database/AFLW2000-3D.zip>AFLW2000 Dataset</a>, which consists of 2000 face images, with some information about them like the facial landmarks and the pitch, yaw, and roll values for each picture.

## Solution:
1. Used the MediaPipe library to extract the face landmarks, then chose the most important facial features (like the nose, forehead, eyes and mouth positions) to be the input of the model.
2. Performed preprocessing step to make the model independent of the face position or scale.
3. Trained a regression model using the position of the most important facial landmarks to estimate the values of the pitch, yaw, and roll.
4. Used rotation, translation, and projection of the axes on the image to visualize the direction the person is looking at.
5. Used the values of pitch, yaw, and roll to define the direction.  
![image](https://user-images.githubusercontent.com/44211916/178109988-79c72995-fdc3-4a96-a8be-10b9288d21aa.png)


## Libraries used:
1. MediaPipe
2. Numpy
3. OpenCV
4. Matplotlib
5. Pandas
6. Scikit-Learn
