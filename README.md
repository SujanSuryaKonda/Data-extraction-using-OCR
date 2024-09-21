# Data-extraction-using-OCR
# BizCardX: Extracting Business Card Data with OCR

## Overview of EasyOCR

EasyOCR is a powerful Python library that simplifies Optical Character Recognition (OCR) for developers. Designed for ease of use, EasyOCR enables the extraction of text from images and scanned documents effortlessly. In this project, we leverage EasyOCR to extract vital information from business cards.

### Key Features of EasyOCR:
- **Simple Installation**: Install with a single pip command.
- **Minimal Dependencies**: Quick and easy configuration of your OCR environment.
- **User-Friendly API**: Importing EasyOCR requires just one line of code, followed by two simple commands to perform OCR.

## Project Overview

BizCardX is an intuitive tool that facilitates the extraction of information from business cards using advanced OCR technology. The extracted data is classified using regular expressions and stored in a SQL database, providing a seamless experience for users through a Streamlit-based graphical user interface (GUI).

### Features:
- **User-Friendly Interface**: Users can easily upload business card images and extract information with just a few clicks.
- **Data Storage**: Extracted information is stored in a structured manner within a MySQL database.
- **Editable Data**: Users can view, modify, and delete stored data as needed.

## Libraries and Modules Used

This project utilizes the following libraries:
- **Pandas**: For creating DataFrames with extracted data.
- **mysql.connector**: To facilitate data storage and retrieval from the database.
- **Streamlit**: For developing an interactive graphical user interface.
- **EasyOCR**: For extracting text from images.

## Workflow

To get started with BizCardX Data Extraction, follow these steps:

1. **Install Required Libraries**: Use the following pip command to install the necessary libraries:

   ```bash
   pip install [library_name]
2. **Run the Application: Execute the main script using Streamlit:

   ```bash
   streamlit run OCR_data.py
3. **Web Interface: A web page will open in your browser featuring three main menu options: HOME, UPLOAD & EXTRACT, and MODIFY. Users can upload business card images for data extraction, storage, and modification.

4. **Data Extraction: Upon uploading a business card, EasyOCR will extract the text, which is then processed by the get_data() function (a custom implementation) to classify details such as:

Company Name
Cardholder Name
Designation
Mobile Number
Email Address
Website URL
Area
City
State
Pin Code
This classification is performed using loops and regular expressions.

Data Display: Classified data is displayed on the screen, allowing users to edit it according to their requirements.

Database Upload: By clicking the Upload to Database button, the extracted data is stored in the MySQL database. (Ensure you provide the correct host, user, password, and database name in the create_database, sql_table_creation, and connect_database functions to establish a successful connection.)

Data Management: Utilize the MODIFY menu to access the uploaded data for read, update, and delete operations.
