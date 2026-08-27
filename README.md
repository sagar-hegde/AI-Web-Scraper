# AI Web Scraper

A Streamlit app that scrapes any website and lets you extract specific information from it using a local LLM (via Ollama + LangChain).

## Features

- Scrape any website using a headless remote browser (Bright Data Scraping Browser) with automatic CAPTCHA solving
- Clean and parse the DOM content into readable text
- Describe what you want to extract in plain English
- Uses `llama3` via Ollama to parse content and return only the requested data

## Tech Stack

- [Streamlit](https://streamlit.io/) – UI
- [Selenium](https://www.selenium.dev/) – browser automation
- [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/) – HTML parsing
- [LangChain](https://www.langchain.com/) + [Ollama](https://ollama.com/) – LLM-based content extraction

## Setup

1. Clone the repo
   ```bash
   git clone https://github.com/sagar-hegde/AI-Web-Scraper.git
   cd AI-Web-Scraper
   ```

2. Install dependencies
   ```bash
   pip install -r requirements.txt
   ```

3. Create a `.env` file with your Scraping Browser endpoint:
   ```
   SBR_WEBDRIVER=your_scraping_browser_websocket_url
   ```

4. Pull the Ollama model
   ```bash
   ollama pull llama3
   ```

## Usage

```bash
streamlit run main.py
```

1. Enter a website URL and click **Scrape Website**
2. View the extracted DOM content
3. Describe what you want to parse and click **Parse Content**
4. View the extracted results
