# Amazon Product Scraper

This repository contains a Selenium-based web scraper designed to extract detailed product information from Amazon. The scraper can navigate through 10 different categories and extract information from up to 1000 products per category, capturing details such as product name, price, description, colors, reviews, and images.

## Features

- **Category Navigation:** have scrapper for each category navigate on Amazon.
- **Product Extraction:** Extract up to 1000 products per category, you can set the limit.
- **Detailed Information:** Capture product name, price, brand, description, colors, reviews, and images.
- **Multi-Color Support:** Extract information for different color variants of each product.
- **Review Extraction:** Collect reviews and ratings for each product variant.
- **Image Collection:** Gather URLs of product images.

## Requirements

- Python 3.x
- Selenium
- Geckodriver (for Firefox)
- Firefox browser
- Fake_useragent
- Concurrent.futures
- Logging

## Libraries Used and Reasons
**Selenium**
- Reason: Selenium is a powerful tool for web browser automation. It allows you to programmatically interact with web elements, which is essential for tasks like filling out search forms, clicking buttons, and navigating through web pages.
**WebDriver**
- Reason: The WebDriver API provides a platform- and language-neutral interface for controlling web browsers. In this project, the Firefox WebDriver (geckodriver) is used to control the Firefox browser.
**Selenium WebDriver Modules**
- webdriver.common.by.By:
Reason: Provides a way to locate elements on the web page using different strategies such as ID, name, XPath, etc.
- webdriver.support.ui.WebDriverWait:
Reason: Allows waiting for a condition to be met before proceeding further in the script, which is useful for ensuring that elements are present before interacting with them.
- webdriver.support.expected_conditions:
Reason: Contains a set of predefined conditions to use with WebDriverWait, making it easier to wait for certain elements or states on the web page.
- selenium.common.exceptions:
Reason: Handles exceptions that might occur during interaction with web elements, such as elements not being found or being stale.
- JSON
Reason: JSON is a lightweight data interchange format that's easy to read and write for humans and machines. It's used here to structure the scraped data and print it in a readable format.
- Time
Reason: The time module is used to introduce delays in the script to ensure that web pages have enough time to load before the script interacts with them. This helps avoid issues where elements are not found because the page hasn't fully loaded.
-Logging
Reason: The logging module provides a flexible framework for emitting log messages from Python programs. It is used here to track the progress and handle any issues that may arise during the scraping process, making debugging easier.
-Concurrent Futures
Reason: The concurrent.futures module provides a high-level interface for asynchronously executing callables using threads or processes. It is used here to handle multiple tasks concurrently, improving the efficiency and speed of the scraping process.
-Fake UserAgent
Reason: The fake_useragent library generates random user-agent strings to mimic different browsers and devices. This helps in avoiding detection and blocking by websites that monitor and restrict access based on user-agent strings.
