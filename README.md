
# OCR Dashboard


A lightweight desktop application for performing Optical Character Recognition (OCR) on images using [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) and Python. Built with PyQt5, this tool allows users to select a folder of images, extract text from each file, preview the results, clean them automatically, and save the output to a file.
ps Python-based program using Tesseract to recognize labels from photos on robot cables.
---

## Features

-  Batch OCR processing of `.png`, `.jpg`, `.jpeg` images
-  Preview extracted text in a scrollable window
-  AutoClean function to filter and format OCR output
-  Save results to `.txt` or `.csv`
-  Close all windows with a single click
-  Local Tesseract integration — no global installation required

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/ocr-dashboard.git
cd ocr-dashboard
2. Install dependencies
bash
pip install pyqt5 pytesseract pillow
3. Add Tesseract OCR
Place a working copy of tesseract.exe and its required .dll files in a folder named tesseract/ inside the project directory. Include the tessdata/ folder with at least eng.traineddata.

Structure:

Код
ocr-dashboard/
├── ocr_dashboard.py
├── preview_window.py
├── icon1.ico
├── tesseract/
│   ├── tesseract.exe
│   ├── libtesseract.dll
│   ├── leptonica.dll
│   ├── ...
│   └── tessdata/
│       └── eng.traineddata
Please, download precompiled binaries from UB Mannheim builds.

Usage
Run the application:

bash
python ocr_dashboard.py
Select a folder containing images.

Choose a file to save the OCR results.

Click "Start OCR" to begin processing.

Preview the results in a separate window.

Optionally use "AutoClean" to filter the output.

Save or close all windows.

Compatibility
Windows 8, 10, 11

Python 3.8+

No internet connection required after setup

License
This project is released under the MIT License.

Код

---

Let me know if you want to add a section for contributing, changelog, or packaging instructions for `.exe`. I can also help you write a localized Slovak version if you'd like to share it with users in your region.
код структура папки
Sure thing, traffic! Here's a clean and logical folder structure for your OCR dashboard project using PyQt5 and Tesseract. This layout keeps things modular, readable, and easy to maintain:

#@@# Project Folder Structure
Код
ocr-dashboard/
                               Entry point for the application
├── OCR_dashboard.py         # Main window with buttons and layout
├── preview_window.py        # Separate window to preview OCR results
├── utils/
│   ├── ocr_engine.py        # Wrapper for Tesseract OCR logic
│   ├── cleaner.py           # AutoClean functions for text processing
│   └── file_manager.py      # File saving and folder handling
├── assets/
│   ├── icon.ico             # App icon
│   └── style.qss            # Optional: custom Qt stylesheet
├── tesseract/
│   ├── tesseract.exe        # Local Tesseract binary
│   ├── libtesseract.dll     # Required DLLs
│   ├── leptonica.dll
│   └── tessdata/
│       └── eng.traineddata  # Language data for OCR
├── README.md                # Project description and setup guide
├── LICENSE                  # License file (e.g., MIT)
└── requirements.txt         # Python dependencies
# Notes
You can run the app via OCR_dashboard.py, which imports and launches the dashboard.

The utils/ folder keeps your logic clean and separated: OCR, cleaning, and file operations.

The assets/ folder is optional but great for icons, stylesheets, or future UI elements.

The tesseract/ folder lets you bundle Tesseract locally so users don’t need to install it globally.

Want help writing the requirements.txt or splitting your code into these modules? I can whip that up for you too.



