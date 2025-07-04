# Utilizing AI-Driven Technology and Geospatial Analysis to Explore Landscape Morphology, Social Vulnerability, and Child Neglect in Los Angeles

This repository contains the code associated with the project entitled **"Utilizing AI-Driven Technology and Geospatial Analysis to Explore Landscape Morphology, Social Vulnerability, and Child Neglect in Los Angeles"** that was presented at **ISUF - Urban Morphology in the Age of Artificial Intelligence** in Torino, Italy, June 2025.

---

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
zsv.run_perception_classification(perception_study='safety')

# Extract features and analyze spatial vulnerability
zsv.extract_features()
zsv.analyze_spatial_vulnerability()
