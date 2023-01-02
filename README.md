# Security-Camera-with-Motion-Alert

Security Camera with Motion Alert Project is a project which is made by taking inspiration from the CCTV camera systems which have become very common now days in almost lane of houses.
This project seems to be very simple but it makes a lot of noise because of its real practical implementation. 


The project consists of only a single python file named Security camera script.py, which is explained in parts as follows.
In the beginning two modules are imported, namely OpenCV (cv2) for image input and image processing, and winsound for making alarm sound.
The whole program just consists of a single function main ().
Inside the function, firstly camera is turned on, then an infinite loop begins to capture the frames continuously.
Inside the loop 2 frames are retrieved consecutively with a fraction of second gap.
Absolute difference of both the frames is calculated and converted to grayscale. Gaussian blur is applied for smoothing the frame.
A binary threshold is applied for brightening the visible moments so that they can be observed with ease.
Then the threshold frame is dilated so that the impression become bold for ease in detection. Using this dilated frame contours are detected.

For each contour if contour area is less 5000px then it is skipped.
If contour area is greater than 5000px then a rectangle is drawn over the contour area and a sound is played using winsound module which was imported earlier.

The final frame is outputted in a frame window.
At last, the loop contains a way to exit loop if Esc or Enter key is pressed, and finally camera is shut down and frame window is destroyed.
