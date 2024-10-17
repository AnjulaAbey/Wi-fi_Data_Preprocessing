# Wi-Fi CSI Data Processing

## Overview
This repository contains a Jupyter notebook for processing Wi-Fi Channel State Information (CSI) data. The primary objective is to extract, clean, and analyze the CSI data for further applications, such as respiratory monitoring using Wi-Fi signals.

## Table of Contents
- [Requirements](#requirements)
- [Data Description](#data-description)
- [Processing Steps](#processing-steps)
- [Results](#results)
- [Usage](#usage)

## Requirements
To run this notebook, ensure you have the following Python libraries installed:

- `pandas`
- `numpy`
- `matplotlib` (for visualization)
- `scikit-learn` (if PCA is used)

You can install these libraries using pip:

```bash
pip install pandas numpy matplotlib scikit-learn
```

## Data Description

The dataset used in this notebook is a CSV file named Val-12BPM.csv, which contains the CSI data for respiratory monitoring. The CSI_DATA column includes raw CSI values interspersed with metadata, which are cleaned for analysis.

## Processing Steps

The main steps in the notebook include:

1. **Loading Data**: The CSV file is loaded using pandas.

2. **Cleaning Data**: The `CSI_DATA` column is processed to:
   - Remove brackets and metadata.
   - Convert the string values to numerical arrays.
   - Skip the first three metadata values for each sample.

3. **Calculating Amplitude**: The amplitude for each CSI sample is calculated using the formula:

   \[
   \text{Amplitude} = \sqrt{\text{Real}^2 + \text{Imaginary}^2}
   \]

4. **Data Visualization**: Various plots are generated to visualize the processed data, including:
   - Amplitude over time.
   - DC-offset removal.
   - Averaging filter application.
   - Bandpass filtered data.
   - Principal component analysis (PCA) results.
   - Welch Power Spectrum Estimate.

## Results

The notebook provides visual outputs that help in understanding the changes made to the CSI data throughout the processing steps. Key plots include:

- Amplitude of Wi-Fi CSI Respiration Data
- Filtered Data (Bandpass)
- Principal Components
- Welch Power Spectrum Estimate

## Usage

To use this notebook:

1. Clone the repository or download the Jupyter notebook file.
2. Open the notebook in Jupyter or any compatible environment.
3. Run the cells sequentially to process the CSI data and generate the visualizations.
