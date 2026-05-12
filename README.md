# Master Thesis Code

This repository contains the code and input data used for my master thesis.

The purpose of the code is to process Excel-based lookahead planning data and analyse weather-related operational constraints using wind and wave data.

## Repository contents

- `Master_Johannes_Ingstad_2026.ipynb`  
  Main Jupyter Notebook containing the analysis code.

- `TIOS case Lookahead Timeplanner Complete.xlsx`  
  Excel input file used by the notebook.

- `README.md`  
  Description of the repository, input data, external data sources and instructions for running the code.

## Code description

The notebook reads operational planning data from the Excel file and processes the relevant rows, columns and time periods.

The code then retrieves weather and marine data from the Open-Meteo API. The weather data are used to analyse whether operational activities are affected by wind and wave conditions.

The analysis includes:

- reading and processing the Excel-based lookahead plan
- extracting relevant operational time windows
- retrieving wind and marine data from Open-Meteo
- comparing weather conditions against operational limits
- identifying weather-related constraints
- producing tables and visualisations used in the master thesis analysis

## Data input

The notebook reads data from the following Excel file:

```python
EXCEL_PATH = "TIOS case Lookahead Timeplanner Complete.xlsx"
```

The Excel file must therefore be located in the same folder as the notebook unless the file path is changed in the code.

## Important note about the Excel input file

The notebook requires the Excel file to be available when the code is run.

If the notebook is run locally, the following two files should be placed in the same folder:

- `Master_Johannes_Ingstad_2026.ipynb`
- `TIOS case Lookahead Timeplanner Complete.xlsx`

If the notebook is opened in Google Colab, the Excel file must be uploaded manually to the Colab session before running the notebook.

## How to run the notebook

1. Download the repository files from GitHub.

2. Make sure the following files are located in the same folder:

   - `Master_Johannes_Ingstad_2026.ipynb`
   - `TIOS case Lookahead Timeplanner Complete.xlsx`

3. Open the notebook file:

   `Master_Johannes_Ingstad_2026.ipynb`

4. Run the notebook cells from top to bottom.

5. If using Google Colab, upload the Excel file to the Colab environment before running the notebook.

## Required Python packages

The notebook uses Python and requires the following packages:

```text
pandas
numpy
matplotlib
altair
requests
openmeteo-requests
requests-cache
retry-requests
openpyxl
```

If any package is missing, it must be installed before running the notebook.

## API and cache

The notebook retrieves weather and marine data from the Open-Meteo API.

The code uses a local cache when retrieving API data. This helps reduce repeated API calls when the notebook is run multiple times.

The cache is generated locally when the notebook is run and is not required to be uploaded to GitHub.

## External data source

Weather and marine data are retrieved from Open-Meteo.

Open-Meteo data are provided under the Creative Commons Attribution 4.0 International license.

Source: Open-Meteo  
License: CC BY 4.0  
Website: https://open-meteo.com/

## Repository purpose

This repository is made publicly available for thesis assessment and reproducibility purposes.

## License

No open-source license is provided for this repository.

The repository is made available for documentation, assessment and reproducibility of the master thesis analysis.
