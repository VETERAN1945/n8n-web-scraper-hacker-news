# Web Scraper & Data Pipeline (n8n + JavaScript + Google Sheets)

## 📌 Project Overview
An automated workflow designed to scrape, clean, and structure data from the Hacker News homepage. The script simulates browser behavior to fetch raw HTML, extracts specific article titles and URLs using CSS selectors, processes the data via JavaScript, and automatically exports the structured entries into a test database (Google Sheets).

## 🛠️ Tech Stack
- **Automation Platform:** n8n
- **Protocols:** HTTP (GET requests)
- **Parsing Techniques:** DOM Parsing, precise CSS selectors (`span.titleline > a`)
- **Data Manipulation:** JavaScript (Node.js / array mapping for merging JSON objects)
- **Integration:** Google Sheets API (OAuth2)

## 🔍 Workflow Architecture & Pipeline Logic
1. **HTTP Request:** Executes a GET request to Hacker News to download the raw HTML source code of the main page.
2. **HTML Extract:** Filters the code using specific CSS selectors. It splits the data flow into two clean, separate arrays: one for article titles and another for URLs.
3. **Code Node (JS):** Normalizes the data structure. It executes a JavaScript map function to merge the isolated arrays into unified JSON objects based on their index pairs.
4. **Google Sheets:** Automatically maps the formatted JSON properties to the corresponding columns (`title` and `link`) and appends them as structured rows into the spreadsheet.

## 🎯 QA & Testing Application
In real-world QA engineering, this automated pipeline is highly valuable for:
- **Data-Driven Testing (DDT):** Quickly gathering and populating QA/test environments with real, dynamic data.
- **Regression Content Monitoring:** Automating checks to ensure that production links are active, properly formatted, and return correct status codes.
<img width="953" height="518" alt="image" src="https://github.com/user-attachments/assets/83876a8a-2b98-4d22-ab65-5cd8b3052575" />
