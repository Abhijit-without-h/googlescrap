# Google Maps Business Scraper

## Disclaimer
This script is intended for educational and research purposes only. The author is not responsible for any misuse of this script. Use it responsibly and at your own risk.

## Overview
This Python script automates the extraction of business information from Google Maps using Playwright. It allows users to select business categories and scrape details such as business name, address, website, phone number, reviews count, reviews average, latitude, and longitude.

## Features
- **Multiple Business Categories**: Choose from a predefined list of business types or add your own.
- **Random City Selection**: Randomly selects cities and states from a provided CSV file (`uscities.csv`).
- **Data Extraction**: Captures comprehensive business details including reviews count and average rating.
- **Data Storage**: Saves scraped data to a centralized CSV file with options to append or overwrite.
- **Duplicate Handling**: Ensures no duplicate businesses are saved.

## Prerequisites
- Python 3.7 or higher
- Playwright (for browser automation)
- Pandas (for data manipulation)
- An included CSV file named `uscities.csv` (should contain at least `city` and `state_id` columns)

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/Noko7/GoogleScraper9000
   ```

2. Navigate to the project directory:
   ```
   cd GoogleScraper9000
   ```

3. Create a virtual environment (optional but recommended):
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows use 'venv\Scripts\activate'
   ```

4. Install dependencies:
   ```
   pip install -r requirements.txt
   playwright install
   ```

## Usage

1. Start the script:
   ```
   python main.py
   ```

2. Select business categories:
   ```
   Select one or more business types by entering their numbers separated by commas or ranges (e.g., 1,3,5-7):
   1. Real Estate companies
   2. Charity/Non-Profits
   3. (etc)...
   ```

3. Follow the prompts:
   - Choose the number of listings you want to capture
   - Start scraping

4. Check the output folder for the scraped data

### Output

- **Directory**: Scraped data is saved in an `output` folder.
- **File**: Data is stored in a centralized CSV file named `Scraped_results.csv`.
- **Data Fields**:
  - `name`: Business name
  - `address`: Physical address
  - `website`: Website URL
  - `phone_number`: Contact phone number
  - `reviews_count`: Number of Google reviews
  - `reviews_average`: Average star rating
  - `latitude`: Geographic latitude
  - `longitude`: Geographic longitude

## Limitations

- **Google Maps Structure Changes**: The script relies on the current structure of Google Maps. Changes to the website may break the script.
- **Rate Limiting and Captchas**: Excessive scraping may trigger Google's anti-bot measures.
- **Geographic Scope**: Currently designed for U.S. cities listed in `uscities.csv`.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.
