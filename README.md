Redbus Webscraping


The "Redbus Data Scraping and Filtering with Streamlit Application" project aims to enhance the transportation sector by automating the collection, analysis, and presentation of bus travel data. Utilizing Selenium for web scraping, this project gathers critical information from Redbus, including bus routes, schedules, ticket prices, and seat availability. By streamlining the data collection process and providing insights through data visualization, this solution helps improve operational efficiency and decision-making in transportation planning.




Problem Statement
This project addresses the challenge of managing and analyzing large volumes of transportation data. By leveraging Selenium for automated data extraction, the "Redbus Data Scraping and Filtering with Streamlit Application" provides an efficient system to gather detailed bus travel information. The solution enables better strategic planning and decision-making by offering tools to analyze and visualize data. This approach enhances operational efficiency within the transportation industry.



Domain
Transportation



Technology Stack
Programming Language: Python 3.12.4
Database: MySQL 8.0
Web Scraping: Selenium
Application Framework: Streamlit



Installed Packages
Selenium: pip install selenium, from selenium import webdriver
Pandas: pip install pandas
Streamlit: pip install streamlit
MySQL Connector: pip install mysql-connector-python
Streamlit-Option-Menu: pip install streamlit-option-menu




Code Flow
1. Redbus.ipynb
Libraries: Imports Selenium, time, and pandas for web automation and data processing.
Browser Initialization: Opens a Chrome browser session.
Page Navigation: Loads the Redbus website and maximizes the window.
Explicit Waits: Sets a 20-second timeout for page elements.
Data Extraction: Retrieves bus route links and names using pagination.
Pagination Handling: Automates navigation across pages to gather all available data.
Data Return: Returns lists containing route names and links.

2. BusDetails.ipynb
Libraries: Imports Selenium, pandas, and time for automation and data handling.
Data Reading: Loads a CSV file containing route data into a pandas DataFrame.
Browser Automation: Opens each route link to extract bus details.
Scroll and Click: Scrolls through each page to reveal bus information and retrieves details like names, schedules, prices, and seat availability.
Data Storage: Appends extracted information into pre-defined lists for further processing.

3. Sql.ipynb
Libraries: Uses pandas for data manipulation and MySQL Connector for database interaction.
Data Preparation: Cleans and formats the extracted data, including converting text to numeric values and handling missing data.
Database Operations:
Creates a MySQL database and table for storing bus details.
Inserts cleaned data into the database.
File Saving: Saves the processed data into a CSV file.

4. RedBus_APP.py
Libraries: Imports Streamlit, pandas, and MySQL Connector for app creation and database management.
Database Connection: Connects to the MySQL database to fetch filtered data.
App Layout: Configures a user-friendly interface using Streamlit with custom headings and styles.
User Interaction:
Provides dropdowns and filters for selecting states, routes, bus types, and price ranges.
Fetches and displays the filtered data based on user inputs.
Data Visualization: Presents the retrieved data in a clear and interactive format for users.




Summary
This project integrates web scraping, data processing, and interactive visualization to streamline transportation data management. By automating repetitive tasks and providing actionable insights, it serves as a valuable tool for stakeholders in the transportation industry.
