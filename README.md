# Virtual-Pointer

It is a virtual mouse based on python using OpenCV library to control mouse through the webcam of your device.

![Alt Text](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExODNkMDc1ZDcwOWFmMDVhZjk2YzkyNDZkYWQ3YzcyMmIwN2QzMDJmMyZjdD1n/r7Y17m4862kdW/giphy.gif)

# Instructions to Run
1. pip install -r requirement.txt
2. Run the python 1.py

(Run on python 3.7)

# Project Description

The code is a Python program that uses computer vision techniques and a mouse controller to allow the user to control the computer mouse with hand gestures captured by a webcam. Here are some of the key features of the code:

- The code imports the necessary libraries, including OpenCV for image processing, NumPy for numerical operations, and pynput for mouse control.
- The program uses the wxPython library to get the size of the display and create a window for displaying the webcam feed and visualizations of the hand gestures.
- The code initializes the webcam by creating a VideoCapture object and setting the resolution to 320x240 pixels.
- The code defines the lower and upper bounds for the green color range in the HSV color space. These values are used to create a binary mask that isolates the green pixels in the image.
- The program uses morphological operations to clean up the binary mask and remove noise.
- The code finds contours in the binary mask and checks if there are two hand gestures present in the image. If two gestures are detected, the program calculates the midpoint between the two gestures and moves the mouse accordingly. The program also draws rectangles around the hand gestures and a line between them to visualize the movement.
- If only one hand gesture is detected, the program treats it as a left-click and moves the mouse to the position of the hand gesture. The program also draws a circle around the hand gesture to visualize the position of the click.
- The program uses a damping factor to smooth the movement of the mouse and make it less jerky.
- The code checks if a pinch gesture is being made and if so, simulates a left-click. The program does this by checking if the area of the combined rectangle around the two hand gestures is within a certain threshold of the area of the outer rectangle that encompasses both gestures. If the area difference is less than 30%, the program simulates a left-click.
- The program updates the position of the mouse in real-time by calling the move method of the mouse controller and passing in the new position. The program also uses a while loop to ensure that the mouse movement is completed before moving on to the next iteration of the loop.
- The program displays the webcam feed and visualizations of the hand gestures using the imshow method of OpenCV. The program also waits for a key press to exit the program.
