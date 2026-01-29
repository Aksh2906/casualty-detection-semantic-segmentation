# UAS-DTU Round 2 – Search and Rescue Task

Name: Aksh Aggarwal
Roll No: 25/A01/023

This project implements the UAS-DTU Round 2 task using Python and OpenCV. The objective is to analyze aerial images from a shipwreck scenario, segment background regions, detect casualties and rescue camps, and assign casualties to camps based on priority and distance.

Task Overview

Segment ocean and land regions from the image

Detect casualties using shape and color

Detect rescue camps (circles)

Assign casualties to camps based on priority score and distance

Compute total priority for each camp

Calculate rescue ratio for each image

Rank images based on rescue ratio

Priority Rules

Star = 3, Triangle = 2, Square = 1

Red = 3, Yellow = 2, Green = 1

Camp capacities: Blue = 4, Pink = 3, Grey = 2

Priority Score = (age priority × emergency priority)

Output

For each image:

[ blue_list , pink_list , grey_list ]
[ priority_blue , priority_pink , priority_grey ]
priority_ratio


Final output:

List of image names sorted by rescue ratio (descending)

Technologies

Python

OpenCV

NumPy

Conclusion

This project demonstrates image segmentation, feature detection, and priority-based decision making for a Search and Rescue scenario.
