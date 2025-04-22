# SMEAR Data API

A Python package for interacting with the SMEAR API and processing data.

## Features
- Fetch time-series data from the SMEAR API.
- Combine data over a range of years.
- Process and clean data for analysis.

## Installation
To install the package locally, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/SMEAR-data-api.git
   cd SMEAR-data-api
   ```

2. Build the package:
   ```bash
   python3 setup.py sdist bdist_wheel
   ```

3. Install the package locally:
   ```bash
   pip install .
   ```

## Usage
After installing the package, you can use it in your Python scripts. Here's an example:

```python
from smear.smear import getData
from utils.data_extract import fetch_combined_data

# Define variables and time range
variables = ['HYY_META.O3672', 'HYY_META.NOx672']
start_year = 1996
end_year = 2023

# Fetch combined data
data_fetched = fetch_combined_data(variables, start_year, end_year)

# Print the fetched data
print(data_fetched)
```

## Directory Structure

```
SMEAR-data-api/
├── smear_api/
│   ├── __init__.py
│   ├── tools.py
├── utils/
│   ├── __init__.py
│   ├── data_extract.py
├── setup.py
├── README.md
├── LICENSE
```

## License
This project is licensed under the Apache License 2.0. See the `LICENSE` file for details.