# Search and Rescue Task

**Author:** Aksh Aggarwal  
**Roll No:** 25/A01/023

---

## Project Summary

This project implements the UAS-DTU Round 2 Search and Rescue task using Python and OpenCV. The objective is to analyze aerial images from a shipwreck scenario to:

- Segment ocean and land regions
- Detect casualties and rescue camps
- Assign casualties to camps based on priority and distance
- Compute priorities and rescue ratios
- Rank images by rescue ratio

---

## Task Overview

For each input image the system performs the following steps:

1. Segment ocean and land regions from the image.
2. Detect casualties using shape and color information.
3. Detect rescue camps (circular markers).
4. Assign casualties to camps based on a computed priority score and distance.
5. Compute the total priority for each camp.
6. Calculate the rescue ratio for the image.
7. Rank all images based on rescue ratio (descending).

---

## Priority Rules

- Shape priority (age proxy):
  - Star = 3
  - Triangle = 2
  - Square = 1
- Emergency priority (color):
  - Red = 3
  - Yellow = 2
  - Green = 1
- Camp capacities:
  - Blue = 4
  - Pink = 3
  - Grey = 2

Priority score for a casualty:
- Priority Score = (age priority × emergency priority)

Assignment goal:
- Place casualties into camps respecting capacities while maximizing total priority handled.

---

## Output Format

For each image the algorithm produces:

- Lists of assigned casualty IDs per camp:
  - [ blue_list , pink_list , grey_list ]
- Total priority per camp:
  - [ priority_blue , priority_pink , priority_grey ]
- Rescue ratio for the image (single numeric value)

Final output (across all images):
- A list of image file names sorted by rescue ratio (descending).

---

## Technologies

- Python
- OpenCV
- NumPy

---

## Conclusion

This project demonstrates image segmentation, feature detection, and priority-based decision-making for a Search and Rescue scenario using aerial imagery. The implemented pipeline segments regions, detects casualties and camps, computes priorities, and ranks images according to rescue effectiveness.

---
