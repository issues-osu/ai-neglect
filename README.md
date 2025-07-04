# Utilizing AI-Driven Technology and Geospatial Analysis to Explore Landscape Morphology, Social Vulnerability, and Child Neglect in Los Angeles
This repository contains the code associated with the project entitled "Utilizing AI-Driven Technology and Geospatial Analysis to Explore Landscape Morphology, Social Vulnerability, and Child Neglect in Los Angeles" that was presented at ISUF - URBAN MORPHOLOGY IN THE AGE OF ARTIFICIAL INTELLIGENCE in Torino, Italy in June 2025.

Installing ZenSVI
This project utilizes the ZenSVI package, a Python package for analyzing street-level spatial vulnerability and social environment. The installation process clones the latest code from the GitHub repository and installs the package along with its dependencies, including geospatial libraries (Shapely, geopandas, contextily), scientific computing (numpy), and machine learning tools (pytorch-lightning).

Installation Command
bash
Copy
pip install git+https://github.com/koito19960406/ZenSVI.git
Basic Usage Example
python
Copy
from zensvi import ZenSVI

# Initialize ZenSVI with your data path
zsv = ZenSVI(data_path="path/to/your/streetview/images")

# Run perception classification (e.g., safety, boring, lively)
zsv.run_perception_classification(perception_study='safety')

# Extract features and analyze spatial vulnerability
zsv.extract_features()
zsv.analyze_spatial_vulnerability()

