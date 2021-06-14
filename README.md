# AI_mouse_hand_gesture

The main objective of the "AI_mouse_hand_gesture" project is automation.
This is a computer vision project that tracks the forefinger and middle finger movement and moves the mouse pointer accordingly on the computer screen.
MediaPipe is a cross-platform framework for building multimodal applied machine learning models using the data avaliable in audio and video format.
The model detects and tracks all the fingers by using the "hand_tracking.py",and the code in this file is written in modular format so that it can be used anywhere by just calling it.
In a single hand the above code can detect and track 21 points.<br>
<image src="hand_landmarks.png" width=500><br> 
Here in this project we are intersted in finding the poistion of "Middle" and the "Index" finger.
All the locations of the fingers are stored in an array.By indexing the position of 4 and 8 we can locate the position of "Thumb" and the "Index" finger.
The location of the index finger is taken as a pointers location and when index finger is moved around, the mouse pointer also moves in the same way.(Note: this time only the index finger should be up and other 4 fingers should be closed down.
Then when middle finger is up it is detected up by the method and returned as both fingers are up.
Then we find the distance between the fingers by using the formula ((x2-x1)^2+(y2-y1)^2)^(0.5).
When this distance between those to becomes less than 40 we assume that a select is made and the that gets reflected on the computer as well.<br><br>
Click [here](https://github.com/Thulasirobocop/AI_mouse_hand_gesture/blob/main/AI_mouse_recordings.mp4?raw=true) to view my recording on this project.
