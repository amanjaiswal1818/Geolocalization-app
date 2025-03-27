# Geolocalization App

## Introduction

This project develops a mobile application for image-based geolocalization. The application estimates the geographic location (latitude and longitude) of a test image by comparing its visual content with that of two training images with known locations. This approach is valuable in scenarios where traditional GPS is unreliable, such as indoor environments or dense urban areas. [cite: 2, 3, 4, 7, 8]

## Key Concepts

* **Geolocalization:** Determining the geographic location of an object using data analysis, in this case, image data. [cite: 2]
* **Image-based Localization:** Estimating location from visual and spatial information extracted from images. [cite: 3]
* **Feature Extraction:** Identifying and extracting distinctive features from images for comparison. [cite: 10]
* **Keypoint Matching:** Finding corresponding features between different images. [cite: 10]
* **Triangulation:** A geometric technique to estimate a point's location using triangles formed from known points. [cite: 15, 16]

## Methodology

The application's location estimation process involves:

1.  **Feature Extraction:** Extracting features from the test image and two training images. [cite: 10]
2.  **Keypoint Matching:** Matching keypoints between the test image and the training images. [cite: 10]
3.  **Location Estimation:** Estimating the test image's location based on the known locations of the training images with the best matches. [cite: 11]

## Algorithms

The project utilizes the following algorithms:

* **SIFT (Scale-Invariant Feature Transform):** A feature detection algorithm robust to scale, rotation, and affine transformations. [cite: 17, 18]
* **AKAZE (Accelerated-KAZE):** An improved keypoint detection and description algorithm for enhanced speed and efficiency. [cite: 19, 20]
* **Triangulation:** A geometric method for determining location using triangles. [cite: 15, 16]

## Mathematical Approach

* **Simple Triangulation:** Calculates the estimated location by averaging the latitudes and longitudes of the training images. [cite: 21]
    * `Latest = (Lattest + Lattrain1 + Lattrain2) / 3`
    * `Lonest = (Lontest + Lontrain1 + Lontrain2) / 3`
* **SIFT-based Triangulation:** Calculates a weighted average of training image locations, weighted by the number of feature matches. [cite: 22, 23]
    * (See presentation for detailed formulas)
* **AKAZE:** Similar to SIFT-based, using normalized similarity scores as weights. [cite: 24, 25]
    * (See presentation for detailed formulas)

## Challenges

The project addresses challenges inherent in image-based geolocalization:

* Lighting variations [cite: 12, 13]
* Perspective changes [cite: 12, 13]
* Occlusions [cite: 12, 13]
* Computational efficiency [cite: 13]

## Expected Outcome

The application provides an estimated latitude and longitude for a given test image. [cite: 14]

## Comparison

The project compares SIFT Triangulation and the AKAZE algorithm, evaluating their performance (e.g., processing time, accuracy). [cite: 26, 27, 28, 29]

## References

* Akaze Algorithm: [https://github.com/pablofdezalc/akaze/blob/master/README.md](https://github.com/pablofdezalc/akaze/blob/master/README.md) [cite: 30]
* Opencv: [https://github.com/opencv/opencv](https://github.com/opencv/opencv) [cite: 30]
* Generative AI Tools Used:
    * [https://chatgpt.com/](https://chatgpt.com/) [cite: 30]
    * [https://claude.ai/](https://claude.ai/) [cite: 30]
    * [https://gemini.google.com/](https://gemini.google.com/) [cite: 30]
    * [https://www.blackbox.ai/](https://www.blackbox.ai/) [cite: 30]
