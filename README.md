# Drone_Surveillance_Python


1. Tello Drone Control:
   - The code utilizes the `djitellopy` library to control a Tello drone.
   - It establishes a connection with the Tello drone and sets initial velocity parameters to zero.
   - The code includes logic for taking off, performing a series of movements (takeoff, rotate, move left), and landing.
   - The Tello's video stream is captured and displayed in a window using OpenCV (`cv2`).
   - It monitors for a 'q' key press to land and exit the program.

2. Color Detection:
   - The script captures video from a camera (possibly an external webcam) and applies color detection techniques.
   - It allows users to adjust HSV (Hue, Saturation, Value) color range thresholds using trackbars.
   - The detected color is isolated, and the result is displayed.
   - Additionally, it applies image processing techniques such as Gaussian blur, Canny edge detection, and contour detection to identify objects in the frame.
   - Detected objects are enclosed in rectangles, and information such as the number of points, area, and direction is displayed on the image.

3. Object Following (Integrated with Tello Control):
   - The code combines color detection and Tello drone control for object following.
   - It tracks an object of the specified color within the camera frame.
   - Based on the object's position relative to the center of the frame, the drone is given velocity commands to follow the object.
   - If the object is to the left, the drone yaws left; if to the right, it yaws right; if above, it moves up; if below, it moves down.
   - The code continually adjusts the drone's velocity based on the object's position, allowing the drone to follow the object.
   - It uses a "dead zone" to avoid small, undesired movements.

4. User Interface:
   - The script creates OpenCV windows for displaying the camera feed and adjusting parameters using trackbars.
   - It stacks multiple images horizontally for easy visualization.

5. Termination:
   - The code terminates drone control and closes OpenCV windows when the 'q' key is pressed.

In summary, this code demonstrates the integration of Tello drone control, color detection, and object following using computer vision techniques. It showcases your ability to work with drones, image processing, and real-time control systems. You can highlight this project on your resume as an example of your skills in robotics, computer vision, and Python programming.
