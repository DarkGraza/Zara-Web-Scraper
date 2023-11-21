# Zara-Web-Scraper
#Zara category IDs scraping
The webscraper uses a headless browser to send requests and catch the JSON response. 
Using a complex for loop, the script grabs all the main collection, category, section codes(1317main codes).
These codes are utilized to construct all API requests and are appended and saved as a csv list.

#Zara product IDs scraping
Then the script uses Async requests through each iteration of list of urls to send requests
Each JSON response from 1317 reponses is saved as a JSON file and then iterated one by one to process information to avoid crashing of Jupyter Lab.

I created a special generator to particularly extract all necessary information from each JSON file.
Then I appended every iteration as a list of dictionaries and saved as csv.
The script collected over 120,000 rows of data.

#Zara Material Scraping
For to scrap each product's material information and its origin data, 
I used to asyncio.sleep() set at 1sec for every 250 requests to avoid my IP getting blocked.
After making for over 120,000 requests for a total of 7hours, the data was collected was 189 columns and 123,000 rows.
Then after careful observation and inferences, I was able to get the columns to 18. 

After much data cleaning all three datasets were saved saved as individual as csv files.
