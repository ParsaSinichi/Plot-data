![output](https://github.com/user-attachments/assets/382866b3-a8ef-403c-97f0-2c1f3c9ee467)# Extracting Data from a Plot Image

## Overview

This project presents a method for extracting data points from a plot image using Python. The technique can be applied when the original data used to generate the plot is unavailable, making it possible to retrieve the underlying data by processing the plot image itself. The process involves image reconstruction, axis extraction, and data scaling, with two different approaches for setting axis limits.

## Table of Contents

1. [Plot Image Generation](#plot-image-generation)
2. [Image Reconstruction](#image-reconstruction)
3. [Axis Extraction and Scaling](#axis-extraction-and-scaling)
    - [Manual Axis Limits](#manual-axis-limits)
    - [Automatic Axis Limits using OCR](#automatic-axis-limits-using-ocr)

## Plot Image Generation

To test the results, we can easily generate random plots and use them as input for the extraction process. Additionally, this method is versatile enough to work with plots found in academic papers or on the internet, allowing for broader application and testing scenarios.


## Image Reconstruction

After the plot image is created, the next step involves reconstructing the image from its pixel data. This involves isolating the key components of the plot, such as the data points or lines, from the background and removing unnecessary parts. 

## Axis Extraction and Scaling

To accurately map the pixel data from the plot image to real-world values, the project offers two methods for setting the axis limits:

### Manual Axis Limits

In the first approach, the user manually sets the limits for the x and y axes. Once the limits are set, the extracted data points are scaled accordingly to match these limits.

### Automatic Axis Limits using OCR

The second approach automates the process of setting axis limits by using OCR (Optical Character Recognition). In this method, the axes are first extracted from the plot image by identifying the largest connected component on the left side of the image. This technique is based on the assumption that the x and y axes are usually located on the left side of the plot and are often connected. After identifying the axes, OCR is applied to read the numerical labels on them. These labels are then used to automatically determine the axis limits, making this method particularly useful when dealing with unknown or difficult-to-determine axis scales.

![output](https://github.com/user-attachments/assets/cd35d8bf-1fbe-4648-a280-1738ae55983a)

