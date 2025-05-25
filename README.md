<!-- Improved compatibility of back to top link -->
<a name="readme-top"></a>

<!-- PROJECT BANNER -->
<h1 align="center">Land Cover and Land Use Classification with Machine Learning</h1>
<p align="center">
  Using K-means clustering to classify land cover types in the United Kingdom from Sentinel-2 satellite imagery.
</p>

---

<!-- TABLE OF CONTENTS -->
<details>
  <summary>📑 Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#background">Background</a></li>
        <li><a href="#the-sentinel-2-satellite">The Sentinel-2 Satellite</a></li>
        <li><a href="#machine-learning-methodology-k-means-clustering">Machine Learning Methodology: K-Means Clustering</a></li>
      </ul>
    </li>
    <li><a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#datasets-used">Datasets Used</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a>
      <ul>
        <li><a href="#references">References</a></li>
      </ul>
    </li>
  </ol>
</details>

---

# About The Project

This project is part of the AI4EO coursework at University College London. It explores the use of unsupervised machine learning for classifying land cover and land use (LULC) based on Sentinel-2 satellite imagery. The algorithm used is K-means clustering, applied to scenes over the United Kingdom.

## Background

Land cover classification is essential for monitoring urbanisation, agricultural patterns, water resources, and forest distribution. With the growing availability of high-resolution remote sensing data, machine learning techniques provide a scalable and automated approach to large-scale LULC mapping. This project applies unsupervised clustering methods to classify different land types — urban, vegetation, and water — over regions of the UK.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## The Sentinel-2 Satellite

Sentinel-2 is a twin-satellite mission by the European Space Agency designed for Earth observation, featuring the Multispectral Instrument (MSI) which captures imagery in 13 spectral bands across visible, near-infrared, and shortwave infrared wavelengths. The 10m, 20m, and 60m spatial resolutions provide diverse data for environmental monitoring and classification.

### Multi-Spectral Instrument (MSI)

The MSI uses a push-broom sensor to record spatially contiguous lines of spectral data. These are later compiled into images that enable the computation of vegetation indices, water indices, and classification models.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Machine Learning Methodology: K-Means Clustering

K-means clustering partitions input data into K groups based on their spectral similarity. Each pixel's reflectance values across selected bands are treated as a feature vector. The algorithm iteratively assigns each pixel to its nearest cluster centroid and updates the centroids until convergence. This method is highly effective for initial unsupervised classification and feature exploration.

![KMeans_Illustration](figures/kmeans_diagram.png)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

# Getting Started

This project is written in Python and designed to run in Google Colab.

## Datasets Used

The dataset consists of Sentinel-2 L2A imagery (surface reflectance), obtained through either the [Copernicus Dataspace](https://dataspace.copernicus.eu/) or Google Earth Engine.

Recommended search parameters for UK coverage:
- Product Type: `S2MSI2A`
- Region: United Kingdom
- Cloud Cover: <10%
- Timeframe: Recent (e.g., 2023–2024)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

# Usage

To reproduce this project:

1. Open `Land_Cover_Classification.ipynb` in [Google Colab](https://colab.research.google.com/).
2. Mount your Google Drive or upload Sentinel-2 image bands.
3. Run all cells sequentially to execute the preprocessing and clustering.
4. Visualise the output classification map.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

# License

This project is distributed under the MIT License. See `LICENSE.txt` for details.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

# Contact

Selina Si – [UCL Crime & Security Science]  
Email: [placeholder@example.com]  
Project Repository: _private submission_

<p align="right">(<a href="#readme-top">back to top</a>)</p>

# Acknowledgments

This project was completed as part of GEOL0069 (AI for Earth Observation) taught by Dr. Michel Tsamados and Weibin Chen at University College London.

## References

- Naushad, R. (2023). Land Cover Classification using Sentinel-2. [GitHub](https://github.com/raoofnaushad/Land-Cover-Classification-using-Sentinel-2-Dataset)
- Sentinel-2 Overview: https://sentinels.copernicus.eu/web/sentinel/missions/sentinel-2/overview
- Unsupervised Learning Guidebook – GEOL0069: https://cpomucl.github.io/GEOL0069-AI4EO/
- IBM. What is unsupervised learning? https://www.ibm.com/topics/unsupervised-learning

<p align="right">(<a href="#readme-top">back to top</a>)</p>
