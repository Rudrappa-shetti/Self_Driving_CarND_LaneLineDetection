# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My Pipeline consists of following steps :

- Conversion of RGB to grascale image .
- Applied Guassian_blur to grayscale image.
- Applied Edge detection on canny images.
- Found the vertices of the mask.
- Applied the vertices and Edged image  to get the masked image.
- Applied Hough transform on masked image to find the line image.
- then drew the lane lines on original image.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

- firstly slope is found for all the lines
- Then the mean is found for all the x and y of all lines
- y = mx +c is used to find the slope and intercepts.
- cv2.line is used to draw the lines	
.
 
### 2. Identify potential shortcomings with your current pipeline

- A sharp U-turn on the road will tough to handle by this algorithm.
- On a curved road the lane lines needs to be drawn as curved.
- A vehicle at the front and lane lines might not work as expected.
- The other symbols on the road like right arrow or left arrow needs be considered,
  since it is currently only straight line.

### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

- the algorithm has to be more flexible as per road scenarios.
- vehicle detection 
- Missing lane line detection 

