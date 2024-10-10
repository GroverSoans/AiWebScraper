AI Web Scraper
Overview
This AI Web Scraper is a Streamlit application designed to scrape websites and extract specific information based on user input. The scraper leverages Selenium for web scraping, BeautifulSoup for HTML content extraction and cleanup, and Ollama LLM for intelligent parsing of the scraped data.

Requirements
Python 3.7+
Streamlit
Selenium
BeautifulSoup
LangChain for integration with the Ollama LLM model
Installation
Clone the repository to your local machine.

bash
Copy code
git clone https://github.com/your-repo/ai-web-scraper.git
Navigate to the project directory.

bash
Copy code
cd ai-web-scraper
Install the required dependencies.

bash
Copy code
pip install -r requirements.txt
Make sure you have the necessary Chrome WebDriver installed and configured. You will need to update the SBR_WEBDRIVER URL with your authentication credentials.

Usage
Start the Streamlit application:

bash
Copy code
streamlit run main.py
In the Streamlit interface:

Enter a website URL in the input field.
Click the "Scrape Site" button to scrape the website. The application will take a screenshot of the website and display the cleaned HTML content.
You can view the DOM content in the expander and optionally input a description of the content you want to extract.
Click "Parse Content" to process the scraped content using the Ollama LLM model, which extracts only the information that matches the provided description.

Features
Scraping: Selenium is used to launch a browser and scrape the website content, taking a screenshot for reference.
Content Cleaning: BeautifulSoup processes the raw HTML, removing scripts and styles to return the cleaned text.
DOM Content Chunking: The DOM content is split into smaller chunks to handle large pages.
Parsing: The scraped and cleaned content can be intelligently parsed based on the user’s input using LangChain's Ollama model.
File Structure
main.py: Main file containing the Streamlit application logic.
scrape.py: Contains helper functions for scraping and cleaning web content.
parse.py: Functionality for parsing content with the Ollama LLM model.
License
This project is licensed under the MIT License.

Author
Grover Soans







