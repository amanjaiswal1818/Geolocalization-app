# Geolocalization App

## Introduction

This project develops a mobile application for image-based geolocalization. The application estimates the geographic location (latitude and longitude) of a test image by comparing its visual content with that of two training images with known locations. This approach is valuable in scenarios where traditional GPS is unreliable, such as indoor environments or dense urban areas.

## Key Concepts

* **Geolocalization:** Determining the geographic location of an object using data analysis, in this case, image data.
* **Image-based Localization:** Estimating location from visual and spatial information extracted from images. 
* **Feature Extraction:** Identifying and extracting distinctive features from images for comparison.
* **Keypoint Matching:** Finding corresponding features between different images.
* **Triangulation:** A geometric technique to estimate a point's location using triangles formed from known points. 

## Methodology

The application's location estimation process involves:

1.  **Feature Extraction:** Extracting features from the test image and two training images.
2.  **Keypoint Matching:** Matching keypoints between the test image and the training images. 
3.  **Location Estimation:** Estimating the test image's location based on the known locations of the training images with the best matches.

## Algorithms

The project utilizes the following algorithms:

* **SIFT (Scale-Invariant Feature Transform):** A feature detection algorithm robust to scale, rotation, and affine transformations. 
* **AKAZE (Accelerated-KAZE):** An improved keypoint detection and description algorithm for enhanced speed and efficiency. 
* **Triangulation:** A geometric method for determining location using triangles. 

## Mathematical Approach

* **Simple Triangulation:** Calculates the estimated location by averaging the latitudes and longitudes of the training images. 
    * `Latest = (Lattest + Lattrain1 + Lattrain2) / 3`
    * `Lonest = (Lontest + Lontrain1 + Lontrain2) / 3`
* **SIFT-based Triangulation:** Calculates a weighted average of training image locations, weighted by the number of feature matches. 
    * (See presentation for detailed formulas)
* **AKAZE:** Similar to SIFT-based, using normalized similarity scores as weights. 
    * (See presentation for detailed formulas)

## Challenges

The project addresses challenges inherent in image-based geolocalization:

* Lighting variations 
* Perspective changes 
* Occlusions 
* Computational efficiency 

## Expected Outcome

The application provides an estimated latitude and longitude for a given test image. 

## Comparison

The project compares SIFT Triangulation and the AKAZE algorithm, evaluating their performance (e.g., processing time, accuracy). 

## References

* Akaze Algorithm: [https://github.com/pablofdezalc/akaze/blob/master/README.md](https://github.com/pablofdezalc/akaze/blob/master/README.md)
* Opencv: [https://github.com/opencv/opencv](https://github.com/opencv/opencv)
* Generative AI Tools Used:
    * [https://chatgpt.com/](https://chatgpt.com/)
    * [https://claude.ai/](https://claude.ai/)
    * [https://gemini.google.com/](https://gemini.google.com/)
    * [https://www.blackbox.ai/](https://www.blackbox.ai/) 
