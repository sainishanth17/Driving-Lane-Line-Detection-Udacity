# **Finding Lane Lines on the Road writeup** 


---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./video_withlines.png "Result"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I used the gaussian blur.

Then I used the canny edge detection. Then I used the function region_of_interest() to get only the area I am interested in.
Then I used hough_lines() fuction for finding the lines. And then I used weighted_img() function for draw lines on initial image.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by averaging the position of each of 
the lines and extrapolate to the top and bottom of the lane.

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the region of interest changed.

Another shortcoming could be the case when position of camera changed our pipeline could not work well.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to find the region of interest dynamically and adapt our pipeline to different positions of the camera.
