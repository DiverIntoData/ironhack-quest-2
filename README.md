
# 🦈 Shark Attacks Data Analysis

## Overview

This project analyzes shark attack incidents worldwide. The dataset is cleaned and validated to ensure accurate country names and coordinates are used for visualization. The analysis culminates in a geographical representation of shark attack incidents, highlighting the countries most affected.

## 📚 Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Data Cleaning Process](#data-cleaning-process)
- [Coordinate Extraction](#coordinate-extraction)
- [Visualization](#visualization)
- [Technologies Used](#technologies-used)
- [License](#license)

## 🛠️ Installation

To run this project, you need to have Python installed along with the required libraries. You can install the necessary libraries using pip:

```bash
pip install pandas numpy openpyxl geopy plotly
```

## 🚀 Usage

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd shark-attacks-data-analysis
   ```

2. Place the dataset file (`GSAF5.xls`) in the project directory.

3. Run the analysis script:
   ```bash
   python your_script_name.py
   ```

4. The final geographical plot will be displayed, showcasing shark attack incidents by country.

## 🧹 Data Cleaning Process

The data cleaning process involves several steps:

- **Loading the Dataset**: The dataset is loaded from an Excel file into a DataFrame.
- **Whitespace Removal**: Leading and trailing whitespace from the `Country` column is stripped.
- **Country Validation**: Regex patterns are used to validate and categorize country names, including:
  - All uppercase letters
  - Proper capitalization
  - Names separated by slashes or ampersands
- **Country Correction**: Common naming issues are addressed (e.g., replacing "&" with "AND").
- **Filtering**: Only valid countries are retained for further analysis.

## 🗺️ Coordinate Extraction

Using the [Nominatim](https://nominatim.org/) API from the `geopy` library, the latitude and longitude of each valid country are extracted. A delay is implemented to respect API rate limits.

## 📊 Visualization

The final analysis is visualized using `plotly`:

- A scatter geo plot displays the number of shark attack incidents per country.
- The top five countries with the most incidents are highlighted for better visibility.

## 🛠️ Technologies Used

- **Python**: The primary programming language.
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical operations.
- **Geopy**: For geographical coordinate extraction.
- **Plotly**: For interactive data visualization.
- **Openpyxl**: For reading Excel files.

## 📜 License

This project is licensed under the MIT License. See the LICENSE file for more details.
