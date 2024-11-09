# 🌍 **StateToVillage: Web Scraper for Geographic Data** 🌍

**StateToVillage** is a powerful web scraper that extracts location-based data from websites, including **states**, **districts**, **tehsils**, and **villages**. This project is designed to collect hierarchical geographic data, structure it in an organized way, and save it for further analysis or reference.

## 🛠️ **Technologies Used:**
- 🐍 **Python**
- 💻 **Selenium WebDriver** for automation
- 🧑‍💻 **BeautifulSoup** for parsing HTML
- 🛠️ **ChromeDriver** for browser interaction
- 🗄️ **JSON** for saving structured data

## 🚀 **Features:**
- 🌐 **Extract States, Districts, Tehsils, and Villages**: Scrape hierarchical location data starting from states down to villages.
- 📥 **JSON Export**: Data is saved in a user-friendly JSON format for easy processing.
- 🤖 **Automated Scraping**: Uses Selenium WebDriver to navigate the website and extract relevant information.
- ⚡ **Efficient Data Fetching**: Optimized for speed and reliability with random delays to simulate natural browsing.

## 📦 **Installation:**
To get started, follow these steps to install the necessary dependencies:

### 1. Clone the repository:
```bash
git clone https://github.com/dharmendradiwaker/StateToVillage.git
cd StateToVillage
```

### 2. Install required packages:
```bash
pip install -r requirements.txt
```

### 3. Install Chromium and dependencies (for headless browsing):
```bash
apt-get update --quiet
apt-get install chromium chromium-driver --quiet
apt-get install chromium -y
apt-get install -y gconf-service libasound2 libatk1.0-0 libcairo2 libcups2 libfontconfig1 libgdk-pixbuf2.0-0 libgtk-3-0 libnspr4 libpango-1.0-0 libxss1 fonts-liberation libappindicator1 libnss3 lsb-release xdg-utils
```

### 4. Install Google Chrome (for the WebDriver):
```bash
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
dpkg -i google-chrome-stable_current_amd64.deb
apt-get -fy install
```

## 💻 **Usage:**

To scrape data, simply run the script with the target URL:

```python
from scraper import get_one_state

url = 'https://vlist.in/'
data = get_one_state(url)
print(data)
```

This will fetch location data from the website and save it to a file called `states_data.json` in a structured format.

### 📊 **Example Output:**
```json
{
  "Andaman and Nicobar Islands": {
    "Nicobars": {
      "Car Nicobar": {
        "Arong": "645015",
        "Big Lapati": "645025"
      },
      "Great Nicobar": {
        "7 km Farm": "645010"
      }
    },
    "South Andaman": {
      "Port Blair": {
        "Aberdeen Bazar": "744101",
        "Anand Bazar": "744103"
      }
    }
  }
}
```

## 🤖 **How it Works:**

1. **WebDriver Setup**: The scraper uses Selenium WebDriver with headless Chrome to navigate the website and extract data.
2. **Data Extraction**: It grabs the state, district, tehsil, and village names from the tables.
3. **Structured JSON Output**: The hierarchical data is stored in a structured JSON format, making it easy to analyze or use in other applications.

## 🧑‍💻 **Contributing:**

We welcome contributions! If you have an idea to improve the scraper or fix bugs, please fork the repository, make changes, and submit a pull request.

### 📝 **Steps to Contribute**:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature-name`).
3. Commit your changes (`git commit -am 'Add feature'`).
4. Push the branch (`git push origin feature/your-feature-name`).
5. Submit a pull request!

### Thank you for using **StateToVillage**! 🌍 Happy scraping! 😊

--- 
