# Raspberry Pi

The raspberry pi uses the PiCamera to detect an aruco marker up to 10 feet away, and collects the pixel locations in the image of all corners of the marker. With this information I calculate the following:
1. Center of the aruco marker in the x-axis in pixels
2. Horizontal angle between the aruco marker and the camera center
3. Distance between the camera and the marker

The horizontal angle between the aruco marker and the camera center is calculated by the ratio of pixels in the image to the FOV of the camera.
The Distance between the camera and the marker is determined by finding the height of the Aruco marker in pixels, and running it through a logarithmic equation determined via interpolation (Excel document provided).

Both of these values are then sent to the Arduino.
