# Lane_detection
Here i am trying to detect the lanes for a particular type of images , which are basically the front cameras of a car
<br>
<br>
Started by reducing the nose and converting to grayscale for easier preprocessing 
<br>
First Task
<br>
Masking the Region of Inerest which for this particular type that is staright line detection i have formed a polygon of a type of trapezium here to incorporate the lane lines w.r.t a car or any vehicle 
<br>
Then i did HoughTransform on the masked image and changing the threshold,minLinelenght and maxLinegap to get a good result after that 
<br>
drew those lines detected on the lane_image
<br>
<br>
Second Task
<br>
To make the image part between the detected lane lines to be black and the rest of the image to be white
<br>
started with sorting the points in lines(from HoughTransform) to left_lane and right_lane and soted them , reason for this is to make the area between 
<br>
the lines defined and be able to make a polygon with those points 
<br>
To sort the points into left and right lane i just used the basic concept of slope as both had opposite sign slope's
<br>
<br>
3rd/Optional Task
<br>
Created a lane mask of the same size as the og/gray image and made White area for lanes, black for background and then applied the mask on the original image to finaly subtract the background
<br>
<br>
For future improvements
<br>
Exploring more algorithms like:--
<br>
Kalman Filter for curved lane detection and is also very prominent for beign able to detect the lanes in night or a foggy environment where the noise is very high and to detect lanes from hough transform or diff algos are very hard.
<br>
Grab Cut which differentiated foreground and background to get the required output
<br>
this algorithm relies heavily on color distribution and gradients to separate foreground from the background , so for environments with lanes being shadowed due to a roadside tress or the road is on a mountain hill creating heavy lightness chnages on the color information of the road could lead to bad results
