# Introduction to Computer Vision – Homeworks (Innopolis University, Fall 2025)

This repository contains my solutions to three homeworks from the “Introduction to Computer Vision” undergraduate course at Innopolis University (Fall 2025). The course gives a practical introduction to core computer vision concepts and their implementation in Python, with a focus on applying CV techniques to real-world problems.

> ⚠️ **Academic honesty / usage notice**  
> All notebooks and code here are my personal coursework solutions. They are provided **only for reference and educational purposes**.  
> If you are taking this or a similar course, **do not copy** these solutions or submit them as your own work.

> ⚠️ **Дисклеймер (по-русски)**  
> Материалы репозитория предназначены **исключительно для ознакомления и в качестве справочного примера**.  
> Пожалуйста, не используйте этот код как готовое решение учебных заданий и не сдавайте его от своего имени.

---

## Repository structure

```text
.
├── hw1
│   └── TUZOV_ARTYOM_HW1.ipynb
├── hw2
│   └── TUZOV_ARTYOM_HW2.ipynb
├── hw3
│   ├── data/
│   │   ├── HumanL.jpg / HumanR.jpg      # stereo pair with a person
│   │   ├── L5.jpg ...  L25.jpg          # left camera images
│   │   └── R5.jpg ...  R25.jpg          # right camera images
│   ├── data.zip                         # archived copy of the data folder
│   └── TUZOV_ARTYOM_HW3.ipynb
├── LICENSE
└── README.md
````

All homeworks are implemented as Jupyter notebooks (`.ipynb`) and use standard Python CV stack (NumPy, OpenCV, Matplotlib).

---

## Homework 1 – Image Filtering & Binary Vision (`hw1/`)

Focus: basic image processing, filtering, and binary vision.

Main ideas and tasks:

* Loading and visualizing images; converting between color and grayscale.
* Implementing 2D convolution “from scratch” and comparing with OpenCV.
* Applying linear filters:

  * box / mean filter,
  * Gaussian smoothing,
  * basic sharpening / unsharp masking.
* Edge detection:

  * gradient computation,
  * Sobel / Laplacian filters,
  * visualization of gradient magnitude and orientation.
* Binary vision:

  * intensity thresholding (fixed, Otsu, etc.),
  * simple morphological operations to clean up binary masks (erosion, dilation, opening/closing).

All code for this homework is in `hw1/TUZOV_ARTYOM_HW1.ipynb`.

---

## Homework 2 – Local Features & Hough Transform (`hw2/`)

Focus: detecting local features and using the Hough transform for geometric structures.

Main ideas and tasks:

* Keypoint detection with classical feature detectors (e.g., Harris / Shi–Tomasi, ORB/SIFT-like features via OpenCV).
* Building local descriptors and matching keypoints between two images.
* Estimating simple geometric transformations (e.g., homography) from matches and visualizing inliers/outliers.
* Using the Hough transform for:

  * line detection in edge maps,
  * (optionally) circle detection.
* Simple object/shape detection pipeline based on edges + Hough transform.

All code for this homework is in `hw2/TUZOV_ARTYOM_HW2.ipynb`.

---

## Homework 3 – Monocular & Stereo Vision (`hw3/`)

Focus: depth from stereo, disparity, and basic monocular geometry.

The `hw3/data/` folder contains:

* `HumanL.jpg`, `HumanR.jpg` – stereo pair with a person.
* `L5.jpg` … `L25.jpg`, `R5.jpg` … `R25.jpg` – pairs of left/right images from a stereo rig.

Main ideas and tasks:

* Working with a calibrated stereo camera pair (left/right images).
* Computing disparity maps using block matching / semi-global matching.
* Converting disparity to depth and estimating distances to selected points in the scene.
* Visualizing epipolar geometry (corresponding points and epipolar lines).
* Using monocular cues and projection equations to reason about scale and distance.

All code for this homework is in `hw3/TUZOV_ARTYOM_HW3.ipynb`.


---

## License

This repository is distributed under the terms of the license specified in `LICENSE`.
Unless explicitly stated otherwise, the license covers only the code and documentation, not any third-party datasets or course materials.
