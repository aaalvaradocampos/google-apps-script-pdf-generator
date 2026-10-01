# 📄 Google Apps Script Formatted PDF Generator

A Google Apps Script designed to automate the mass generation of official certificates and documents. This script not only replaces placeholders with data from Google Sheets but also programmatically applies strict formatting rules (like bolding specific words and justifying paragraphs) before exporting the final output as an organized PDF.

## ✨ Features

- **🎨 Advanced Text Formatting:** Automatically replaces placeholder tags and applies strict bold formatting *only* to the newly inserted data, preserving the rest of the document's style.
- **📏 Programmatic Alignment:** Finds specific paragraphs within the Google Doc template and forces a 'Justified' horizontal alignment to meet official document standards.
- **📂 Smart Nested Organization:** Automatically categorizes users by their specialty/status and dynamically creates a nested folder structure (`Main Folder > Specialty > PDF`) in Google Drive to store the files.
- **🖨️ Automated PDF Export:** Converts the processed Google Docs into immutable PDF files directly in the cloud.
- **🔍 Conditional Filtering:** Processes only the rows that match a specific criteria (e.g., a specific graduation date or event).

## 🚀 Setup & Installation

1. Open your Google Sheet containing the student/user data.
2. Navigate to **Extensions > Apps Script** in the top menu.
3. Delete any existing code in the editor and paste the contents of `generador_constancias.js`.
4. Update the **Configuration Variables** at the top of the script (see below).
5. Click the **Save** icon.
6. Run the `generadorConstanciasEstandarizadas` function. Grant the necessary permissions to Google Apps Script the first time you execute it.

## ⚙️ Configuration

Before running the script, update the following placeholder variables at the top of the code with your actual Google Drive/Sheets IDs:

```javascript
const SPREADSHEET_ID = 'YOUR_SPREADSHEET_ID_HERE'; // The ID of your Google Sheet
const TEMPLATE_ID = 'YOUR_TEMPLATE_DOC_ID_HERE'; // The ID of your Google Doc template
const FOLDER_DESTINO_ID = 'YOUR_DRIVE_FOLDER_ID_HERE'; // The ID of the root destination folder
