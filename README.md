1- I have downloaded Python 3.9.6 for windows, from https://www.python.org/downloads/

2- In my Command Prompt I wrote the following command to make sure python was working:

python --version 

3- Downloading OpenCV packages using the following command:

pip install opencv-python

![image](https://user-images.githubusercontent.com/85526390/128372318-fdf27c0f-4d25-4907-ab74-33f808660fe5.png)

3- In my text editor, I have wrote the following code:

import cv2

cap = cv2.VideoCapture(0)

while True:

    ret, frame =cap.read()

    cv2.imshow('frame', frame)
    cv2.waitKey(1) #This line is for waiting 1ms before going to the next frame.
    
4- Then I have downloaded the Haar Cascade zip file from the following link:

https://drive.google.com/file/d/1pomC9Zw178nxgNOrpemaQfSH8rSVyMBD/view









