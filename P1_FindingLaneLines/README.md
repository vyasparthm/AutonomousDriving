# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />
<table style="width:100%">
  <tr>
    <th>
      <p align="center">
           <a href="https://youtu.be/Zi-lfy7a8tg"><img src="./test_videos_output/solidYellowLeft.gif" alt="Overview" width="40%" height="40%"></a>
           <br>P1: Finding Lane Lines Yellow Lane
           <br><a href="./FindingLaneLines.ipynb" name="p1_code">(code)</a>
      </p>
    </th>
     <th><p align="center">
           <a href="https://youtu.be/EQkBjCXejfc"><img src="./test_videos_output/solidWhiteRight.gif" alt="Overview" width="40%" height="40%"></a>
           <br>P1: Finding Lane Lines White Lane
           <br><a href="./FindingLaneLines.ipynb" name="p1_code">(code)</a>
        </p>
    </th>
 </table>
Overview
---

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project you will detect lane lines in images using Python and OpenCV.  OpenCV means "Open-Source Computer Vision", which is a package that has many useful tools for analyzing images.  


Writeup about this project
---


**1. The pipeline:** <br />
    The Pipeline in this project depends on draw_lines() Function, which is the essential part and ultimate goal of the project.
This  function draws `lines` with `color` and `thickness`. Lines are drawn on the image inplace (mutates the image). Basically, we take the test images provided by Udacity, then we simpaly show them in Masked, formatted with Hough Lines and combine everything to show detected Lane lines on those images. Once that part is take care of, we use the two provided videos solidWhiteRight.mp4 and solidYellowLeft.mp4 and use our pipeline to draw lines on the video.

**2. Shortcomings:** <br />
    This is a simple lane detection pipeline, and as such it has a number of potential shortcomings.
First, since we are fitting lines (not curves) to the lane lines, this pipeline may yield poor results on urban roads with sharp turns.  Second, it may struggle when there are signs in the road, such as arrows, crosswalks, or or words (e.g., "do not block"). It may also  struggle when there are double lane lines (i.e., "do not cross" lines). This pipeline may not be robust to different lighting. Finally, it  would probably have difficulty when there are a lot of cars on the road and the lane lines cannot be seen 100+ feet in front of the car.

**3.Possible improvements:** <br />
    To more accurately detect the lane lines, it would be beneficial to fit a nonlinear curve to the lanes (such as a spline), instead of fitting a line. <br />

One issue that can be seen in the videos is that the lane lines sometimes jump around. To obtain smoother results, we could incorporate information from the previous frame(s) when detecting lanes in the current frame.

The Shortcomings and improvements ideas are inspired from the work of: 
[Jeff Irion](https://jefflirion.github.io/udacity_car_nanodegree_project01/index.html)


My videos: [solidWhiteRight](https://youtu.be/EQkBjCXejfc) ,[solidYellowLeft](https://youtu.be/Zi-lfy7a8tg).

The Project
---

## If you have already installed the [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) you should be good to go!   If not, you should install the starter kit to get started on this project. ##

**Step 1:** Set up the [CarND Term1 Starter Kit](https://classroom.udacity.com/nanodegrees/nd013/parts/fbf77062-5703-404e-b60c-95b78b2f3f9e/modules/83ec35ee-1e02-48a5-bdb7-d244bd47c2dc/lessons/8c82408b-a217-4d09-b81d-1bda4c6380ef/concepts/4f1870e0-3849-43e4-b670-12e6f2d4b7a7) if you haven't already.

**Step 2:** Open the code in a Jupyter Notebook

You will complete the project code in a Jupyter notebook.  If you are unfamiliar with Jupyter Notebooks, check out [Udacity's free course on Anaconda and Jupyter Notebooks](https://classroom.udacity.com/courses/ud1111) to get started.

Jupyter is an Ipython notebook where you can run blocks of code and see results interactively.  All the code for this project is contained in a Jupyter notebook. To start Jupyter in your browser, use terminal to navigate to your project directory and then run the following command at the terminal prompt (be sure you've activated your Python 3 carnd-term1 environment as described in the [CarND Term1 Starter Kit](https://github.com/udacity/CarND-Term1-Starter-Kit/blob/master/README.md) installation instructions!):

`> jupyter notebook`

A browser window will appear showing the contents of the current directory.  Click on the file called "P1.ipynb".  Another browser window will appear displaying the notebook.  Follow the instructions in the notebook to complete the project.  

**Step 3:** Complete the project and submit both the Ipython notebook and the project writeup


For more exciting videos about technology, please do not forget to subscribe to my [YouTube Channel](https://www.youtube.com/channel/UCqxm7CkItJsJk6ME8qn_bAA/featured)
