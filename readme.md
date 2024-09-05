# Satellite Image Segmentation using SAM (Segment Anything Model)

This project demonstrates the use of the Segment Anything Model (SAM) for automated object segmentation in satellite imagery. It utilizes the `segment-geospatial` library to perform image segmentation and visualization.

## Overview

The notebook performs the following main tasks:

1. Downloads and processes a satellite image for a specific area.
2. Applies the SAM model to generate object masks and annotations.
3. Visualizes the results using various mapping and comparison techniques.
4. Converts the segmentation results to vector format.

## Key Components

- **Leafmap**: Used for interactive map visualization and satellite image acquisition.
- **SamGeo**: A wrapper around the SAM model, tailored for geospatial applications.
- **Image Processing**: Includes downloading satellite imagery and converting TMS to GeoTIFF.
- **Visualization**: Utilizes matplotlib and leafmap for displaying results and comparisons.

## Workflow

1. **Setup**: Install required libraries and import necessary modules.
2. **Map Initialization**: Create an interactive map centered on the area of interest.
3. **Image Acquisition**: Download a satellite image for the selected area.
4. **SAM Model Initialization**: Set up the SAM model with appropriate parameters.
5. **Mask Generation**: Apply the SAM model to generate object masks.
6. **Visualization**: Display the generated masks and annotations.
7. **Comparison**: Compare the original image with the segmentation results.
8. **Vector Conversion**: Convert raster masks to vector format.
9. **Advanced Segmentation**: Perform automatic mask generation with custom parameters.

## Key Functions and Classes

- `SamGeo`: Main class for applying the SAM model to geospatial data.
- `leafmap.Map`: Creates interactive maps for visualization.
- `leafmap.tms_to_geotiff`: Converts TMS (Tile Map Service) to GeoTIFF format.
- `leafmap.image_comparison`: Provides side-by-side comparison of images.

## Results

The notebook generates several output files:

- `satellite.tif`: Downloaded satellite image
- `masks.tif` and `masks2.tif`: Generated object masks
- `annotations.tif` and `annotations2.tif`: Visualizations of the segmentation results
- `masks.gpkg`: Vector format of the segmentation results

## Usage

To run this notebook:

1. Ensure you have the required libraries installed (`segment-geospatial`, `leafmap`).
2. Execute the cells in order, following any interactive steps for map navigation.
3. Adjust parameters in the `sam_kwargs` dictionary for custom segmentation behavior.

## Note

This notebook requires a CUDA-capable GPU for optimal performance when running the SAM model.