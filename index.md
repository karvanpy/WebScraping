# Welcome to the WebScraping Pages!
Just because i don't like typing the same code again and again for doing Web Scraping even a simple website, so i made this!
***
Don't let their websites detect you as a bot! **Make your scraper like hooman instead!**
```python
HEADERS = {
	'sec-ch-ua': '"(Not(A:Brand";v="8", "Chromium";v="99", "Google Chrome";v="99"',
	'sec-ch-ua-platform': "Linux",
	'sec-fetch-dest': 'empty',
	'sec-fetch-mode': 'cors',
	'sec-fetch-site': 'same-origin',
	'user-agent': 'Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/99.0.4844.35 Safari/537.36'
}
```
## Scraping with Selenium
The ammunition:
```python
import json
from bs4 import BeautifulSoup
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.chrome.options import Options
```
Setup the target
```python
url = "https://books.toscrape.com/"
```
Create the option if we want custom the weapon (for example: headless browser, window size, etc...)
```python
options = Options()
options.headless = True
```
Apply custom setting to webdriver
```python
driver = webdriver.Chrome(options=options)
driver.get(url)
```

Get the target resource to the HTML format
```python
content = driver.page_source
```

Play it with BeautifulSoup!
```python
soup = BeautifulSoup(content, "html.parser")
```
