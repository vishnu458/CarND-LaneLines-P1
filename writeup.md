# **Finding Lane Lines on the Road** 

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report



---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of the below steps. 
First, I converted the images to hls, then I applied canny function to that image. Then I obtained the quadrilateral region of the lanes and applied hough transform to the resulted image.

In order to draw a single line on the left and right lanes, I added a filtering function to filter out the line segments obtained from houghLinesP function in draw_lines() function. Lines on the left half of the image with -0.5 to -0.8 were segregated and averaged out to get the lane line on the left. Lines on the right half of the image with 0.5 to 0.8 were segregated and averaged out to get to get the lane line on the right.



### 2. Identify potential shortcomings with your current pipeline

* The pipeline has not been tested with vehicles at the front of ego vehicle.
* The pipeline may not be accurate with night time driving videos.
* The pipeline may not work if there are markings on the road (like stop sign)


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to use hough transform that can follow the road curvature
