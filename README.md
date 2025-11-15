# Intelligent-Document-Automation-Smart-OCR-Bot

Project Description
This project demonstrates an approach for extracting structured key-value information (like company name, date, total amount) from receipt and invoice images. It uses a combination of Optical Character Recognition (OCR) and the Google Gemini multimodal model for robust information extraction.

The workflow includes:

Downloading the SROIE dataset.

Preprocessing images using OpenCV for better OCR results.

Extracting text from the images using Tesseract OCR (pytesseract).

Using the Gemini API to analyze both the original image and the OCR-extracted text, and outputting the structured data in JSON format.

Screenshot/Example
<img width="310" height="631" alt="Screenshot 2025-11-15 at 9 14 44 PM" src="https://github.com/user-attachments/assets/2bf3f04b-68a6-4cde-bb3a-bfd5921d395d" />


Prerequisites
To run this project, you need:

A Google Gemini API Key.

A Kaggle account to download the dataset (if running outside the provided notebook environment).

Setup and Dependencies
The required packages can be installed using pip.

Bash

!pip install -qU kagglehub pandas google-genai opencv-python-headless pytesseract
The notebook also assumes Tesseract OCR is installed and accessible in the environment.

Usage
Set up your API Key: Ensure your Gemini API key is configured as an environment variable or passed directly to the client.

Download Dataset: The notebook automatically downloads the urbikn/sroie-datasetv2 from Kaggle Hub.

Run the Notebook: Execute the cells in the L16.ipynb notebook sequentially.

The notebook will iterate through the image files.

For each image, it performs image processing, OCR, and then calls the Gemini API.

The extracted JSON information will be saved to a specified output directory.

Data Source
The dataset used in this notebook is the SROIE datasetv2 (Scanned Receipt OCR and Information Extraction).

Source: urbikn/sroie-datasetv2 on Kaggle Hub.

Content: Contains various receipt and invoice images (.jpg files).
