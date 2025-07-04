## Utilizing AI-Driven Technology and Geospatial Analysis to Explore Landscape Morphology, Social Vulnerability, and Child Neglect in Los Angeles

This repository contains the code associated with the project entitled **"Utilizing AI-Driven Technology and Geospatial Analysis to Explore Landscape Morphology, Social Vulnerability, and Child Neglect in Los Angeles"** that was presented at **ISUF - Urban Morphology in the Age of Artificial Intelligence** in Torino, Italy, June 2025.

## Project Overview

This repository implements a complete workflow using **ZenSVI**, a Python toolkit for street-level spatial vulnerability and social environment analysis. The key steps include:

- **Downloading** street-level images from Mapillary using a geographic shapefile as input.
- **Segmenting** the images into meaningful visual components with computer vision techniques.
- **Classifying perception** attributes (e.g., safety, depression) on segmented images using AI models.
- **Extracting** pixel-level ratios and reshaping the data into wide-format tables suitable for analysis.
- **Merging** image metadata with geographic coordinates to enable spatial mapping.
- **Visualizing** spatial patterns of environmental and social indicators such as vegetation coverage.
- **Exporting** data as CSV and GeoJSON files, ready for GIS software and further spatial/statistical analysis.

The workflow supports GPU acceleration (e.g., via Google Colab) for efficient processing of large image datasets. It integrates advanced geospatial libraries including geopandas and h3 for multi-scale spatial aggregation and visualization.

---

### Requirements & Setup

- Python 3.11+
- GPU-enabled environment recommended (e.g., Google Colab Runtime → Change runtime type → GPU)
- Dependencies installed via:
  
  ```bash
  pip install git+https://github.com/koito19960406/ZenSVI.git
---
## Using GPU Acceleration and Google Colab

To speed up processing and handle large datasets efficiently, this project supports GPU acceleration, which is especially useful for machine learning tasks like perception classification.

We recommend running the code on **Google Colab**, which provides free access to GPUs and an easy-to-use cloud environment. The Colab notebook is pre-configured with the necessary dependencies and allows you to upload your Street View image data, run ZenSVI’s models on GPU, and visualize results without local hardware constraints.

Using GPU significantly reduces runtime compared to CPU-only environments, enabling faster feature extraction and vulnerability analysis. For best performance, ensure you enable GPU acceleration in the Colab runtime settings:

`Runtime > Change runtime type > GPU`

## Installing ZenSVI

This project uses [ZenSVI](https://github.com/koito19960406/ZenSVI), a Python package for street-level spatial vulnerability and social environment analysis.

The installation process clones the latest code from the GitHub repository and installs the package along with its dependencies, including geospatial libraries (`Shapely`, `geopandas`, `contextily`), scientific computing (`numpy`), and machine learning tools (`pytorch-lightning`).

> **Note:** Some warnings about version mismatches (e.g., `protobuf`, `numpy`) may appear during installation. These are common in complex Python environments and usually do not affect package functionality.

### Installation Command

```bash
pip install git+https://github.com/koito19960406/ZenSVI.git

from zensvi import ZenSVI

# Initialize ZenSVI with your data path
zsv = ZenSVI(data_path="path/to/your/streetview/images")

# Run perception classification (e.g., 'safety', 'boring', 'lively')
classifier = ClassifierPerception(perception_study=indicator)
