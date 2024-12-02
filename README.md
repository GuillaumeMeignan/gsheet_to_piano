# Google Sheets to API Integration

This Google Apps Script project allows you to fetch data from a Google Sheet, and send it to Piano Analytics.

## Installation and Setup

### 1. Open Apps Script in Google Sheets
1. Open your Google Sheet.
2. Go to **Extensions > Apps Script** in the menu bar.

### 2. Import the Code
1. Copy the provided code from this repository.
2. Paste it into the Apps Script editor.

### 3. Configure API Variables
- Open the Apps Script editor and locate the following variables:
  - **`apiKey`**: Set your API key for authorization (this is shared across both APIs).
  - **`apiUrl`**: The endpoint URL depends on the type of data you want to send:
    - For enrichment data, set the URL to your enrichment API endpoint.
  - **`siteId`**: For measurements data, set the site ID corresponding to your project or site.
  - **`measurementKey`**: For measurements data, set the key identifying the measurement context.

### 4. Save the Script
- Click the **File > Save** option in the Apps Script editor.

### 5. Import Macros into Google Sheets
1. Return to your Google Sheet.
2. Go to **Extensions > Macros > Import Macros**.
3. Select the functions `pianoEnrichmentAPIwithGsheet` and `pianoMeasurementsAPIwithGsheet`.
4. Assign the macros to buttons in your Google Sheet (optional).

## How to Use

### Enrichment API
1. Populate your Google Sheet with the required data for enrichment.
2. Ensure that `apiUrl` points to your enrichment API endpoint.
3. Run the macro `pianoEnrichmentAPIwithGsheet` to send data to the enrichment API.

### Measurements API
1. Populate your Google Sheet with the required data for measurements.
2. Ensure that:
   - `siteId` and `measurementKey` are set correctly for your measurements project.
3. Ensure your sheet has the following format:
   - `date` column for periods.
   - Columns starting with `m_` for metrics.
   - Other columns for properties.
4. Run the macro `pianoMeasurementsAPIwithGsheet` to send data to the Measurements API.

## Error Handling
- If an error occurs, an alert will pop up in Google Sheets.
- Check the logs in the Apps Script editor (**View > Logs**) for detailed error messages.

## Contributing
Feel free to contribute by submitting issues or pull requests to enhance this project.

## License
This project is open-source and created by Kimetrix
