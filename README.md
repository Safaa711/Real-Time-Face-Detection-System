1- I have downloaded Python 3.9.6 for windows, from https://www.python.org/downloads/

2- In my Command Prompt I wrote the following command to make sure python was working:

python --version 

3- Downloading OpenCV packages using the following command:

pip install opencv-python

![image](https://user-images.githubusercontent.com/85526390/128372318-fdf27c0f-4d25-4907-ab74-33f808660fe5.png)

3- Then I have downloaded Haar Cascade:

https://github.com/Safaa711/Real-Time-Face-Detection-System/blob/main/haarcascades.zip

4- In my text editor, I have written the following code: 


    import cv2
    
    cascade_classifier = cv2.CascadeClassifier('haarcascades/haarcascade_frontalface_alt.xml')

    cap = cv2.VideoCapture(0)

    while True:
   
     ret, frame = cap.read()
  
     gray = cv2.cvtColor(frame, 0)
   
      detections = cascade_classifier.detectMultiScale(gray,scaleFactor=1.3,minNeighbors=5)
  
      if(len(detections) > 0):
    
        (x,y,w,h) = detections[0]
        
        frame = cv2.rectangle(frame,(x,y),(x+w,y+h),(255,0,0),2)

    # for (x,y,w,h) in detections:
    
    # 	frame = cv2.rectangle(frame,(x,y),(x+w,y+h),(255,0,0),2)

    # Display the resulting frame
    
    cv2.imshow('frame',frame)
    
    if cv2.waitKey(1) & 0xFF == ord('q'):
    
        break
        
        cap.release() 
        cv2.destroyAllWindows()

The result:

![Screenshot (117)](https://user-images.githubusercontent.com/85526390/128439288-6ad7833f-c0a9-4b77-9baa-1af01fa6d767.png)

![Screenshot (118)](https://user-images.githubusercontent.com/85526390/128439316-23d409fa-2c9b-465b-8046-b84af0c432e8.png)











