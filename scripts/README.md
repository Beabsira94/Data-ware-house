# Telegram Scraping for Ethiopian Medical Business Data

## Overview

This project implements a data scraping solution to extract messages and media from Telegram channels relevant to Ethiopian medical businesses. The goal is to collect data from specified channels, including text messages and associated media, to enable further analysis of market trends and business activities in the medical sector. The project uses the **Telethon** library to interact with Telegram's API and handle the scraping process.

## Key Features

1. **Telegram Client Setup**:

   - The project utilizes the `Telethon` library to connect to Telegram channels and retrieve messages. The API credentials, including `api_id`, `api_hash`, and `phone`, are securely loaded from a `.env` file.
2. **Scraping Process**:

   - The scraping function iterates through messages in each specified channel, downloading text and media files, including images and documents. The media is stored locally in the `photos/` directory, and detailed logs track the scraping process.
3. **Storing Data in CSV Format**:

   - Data from each channel is stored in a separate CSV file, containing columns such as `Channel Title`, `Channel Username`, `Message ID`, `Message Text`, `Date`, and `Media Path`. This structure ensures easy access and further analysis of the scraped data.
4. **Logging and Error Handling**:

   - The project implements comprehensive logging, saving logs in a `scraping.log` file. The log captures important details, such as message processing, media downloads, and errors during the scraping process, providing transparency and easy debugging.
5. **Channel Management**:

   - Channels to be scraped are loaded from a `channels.json` file. The project is flexible enough to handle multiple channels, and it allows for future expansion by easily adding or removing channels from the JSON file. Comments can also be stored in the JSON file, though they are logged separately.

## How to Use

1. **Setup**:

   - Install the required dependencies:
     ```bash
     pip install telethon python-dotenv
     ```
   - Create a `.env` file with your Telegram API credentials (`TG_API_ID`, `TG_API_HASH`, and `phone`).
2. **Run the Scraper**:

   - Customize the `channels.json` file with the Telegram channels you want to scrape. Then, run the script:
     ```bash
     python scraper.py
     ```
3. **Output**:

   - Scraped data will be saved in CSV files, one for each channel. Media files will be downloaded to the `photos/` directory.
4. **Logs**:

   - Check the `scraping.log` file for detailed logs of the scraping process, including any errors or media download status.

## Conclusion

This project offers an efficient way to collect data from Telegram channels for Ethiopian medical businesses, with support for handling multiple channels, storing data in structured CSV files, and maintaining detailed logs for monitoring. It is scalable, customizable, and can be extended to handle additional business use cases or channels.
