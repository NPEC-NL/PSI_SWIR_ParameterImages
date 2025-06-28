# PSI Hyperspectral Image Processing
This repository contains a Google Colab notebook for preprocessing and extracting key vegetation-related indices from hyperspectral images captured with PSI SWIR (Short-Wave Infrared) cameras.

## 📂 Structure of the Repository
The repository is organized into two separate Google Colab notebooks, each designed for a different use case:

**1. Tutorial – Single Image Example**
Notebook: PSI_Hyperspectral_Example.ipynb
This is a step-by-step tutorial for working with a single hyperspectral image. It helps users understand how the calibration and index computation works.
📌 Recommended for:
First-time users
Learning and debugging
Testing with a single PSI measurement

**2. Batch Processing – Multiple Images**
Notebook: PSI_Hyperspectral.ipynb
This notebook is designed to automatically process a folder containing multiple PSI hyperspectral measurements. It reads corresponding raw, white, and dark calibration files and outputs vegetation index maps (as .tiff images).
📌 Recommended for:
Processing large datasets
Running full experiments
Generating index outputs for multiple field acquisitions


## 🌱 What This Notebook Does
The notebook processes hyperspectral .bil data files, applying radiometric calibration using associated dark and white reference images. It then calculates several plant-related indices:

NDWI – Normalized Difference Water Index

MSI – Moisture Stress Index

NDII – Normalized Difference Infrared Index

Band @ 1000 nm – Extracted calibrated reflectance slice

All outputs are saved as .tiff files for further analysis or visualization.

## 🛠 How to Use This Tutorial Notebook
1. Open the notebook in Google Colab
Click below to open directly in Google Colab:

[Open tutorial in Colab](https://github.com/NPEC-NL/PSI_SWIR_ParameterImages/blob/main/Tutorial_%E2%80%93_Single_Image_Example.ipynb)

2. Make a copy to your own Google Drive
Go to:
File > Save a copy in Drive

3. Upload or Mount Your Data
You can:

Upload .bil files directly

Or mount your Google Drive (/content/drive/MyDrive/...) containing your PSI hyperspectral data

Each measurement group must include:

*_Data.bil (Raw data)

*_Dark.bil (Dark reference)

*_White.bil (White reference)

4. Set input and output folders
Edit these variables in the notebook:

python
Copy
Edit
PATHinput = 'your_input_folder_path/'
PATHoutput = 'your_output_folder_path/'
FILE_NAME_key = 'SWIR'
5. Run the cells
Run the notebook from top to bottom. It will:

Automatically group related files

Calibrate raw images

Compute the indices

Save each output as .tiff images

## ✅ Output
For each image group, you’ll get:

groupname_ndwi.tiff

groupname_msi.tiff

groupname_ndii.tiff

groupname_wl1000.tiff

## ❓ Need Help?
If you encounter any issues or have questions, feel free to open an issue or contact the author.

## Happy hyperspectral processing!

