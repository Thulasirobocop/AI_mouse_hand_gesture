# AI_mouse_hand_gesture

The main objective of the "Gesture_volume_control" project is automation.
This is a computer vision project that automatically adjusts the speaker volume using hand gestures.
MediaPipe is a cross-platform framework for building multimodal applied machine learning models using the data avaliable in audio and video format.
The model detects and tracks all the fingers by using the "hand_tracking.py",and the code in this file is written in modular format so that it can be used anywhere by just calling it.
In a single hand the above code can detect and track 21 points.
<image src="hand_landmarks.png" width=500><br> 
Here in this project we are intersted in finding the poistion of "Thumb" and the "Index" finger.
All the locations of the fingers are stored in an array.By indexing the position of 4 and 8 we can locate the position of "Thumb" and the "Index" finger.
Then we find the distance between the fingers by using the formula ((x2-x1)^2+(y2-y1)^2)^(0.5).
The "Pycaw" library has a method called "volume.SetMasterVolumeLevel()" by which, we can adjust the computer's speaker volume
We find the minimum and maximum range of the volume and then we map the distance value with minimum and maximum range of the volume
Then depending upon the distance, the speaker volume is adjusted.
