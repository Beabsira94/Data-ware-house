# Ethiopian Medical Businesses Data Warehouse

## Overview

This project, commissioned by Kara Solutions, focuses on building a data warehouse to store data on Ethiopian medical businesses scraped from Telegram channels. The primary goal is to develop a scalable, robust system capable of collecting, processing, and storing data for efficient analysis and reporting. By centralizing the data in a warehouse, we can conduct comprehensive analyses to uncover valuable insights and trends in the Ethiopian medical business landscape.

## Key Components

### 1. Data Scraping and Collection Pipeline

The first task involved extracting data from public Telegram channels, such as DoctorsET and Chemed, using the **Telethon** Python package. This included scraping text data, images, and other relevant content. The scraped data was temporarily stored and monitored through logging to ensure smooth extraction and timely error tracking.

### 2. Data Cleaning and Transformation

Once the data was collected, the next step was to clean and transform it. This involved removing duplicates, handling missing values, and ensuring standardized formats for consistency. Data Build Tool (**DBT**) was used for performing data transformations and ensuring data quality before loading the cleaned data into the data warehouse.

### 3. Object Detection Using YOLO

To enhance the analysis of the scraped data, we integrated **YOLO (You Only Look Once)**, an object detection model. YOLO was used to detect and classify objects in images scraped from Telegram channels, enabling deeper insights into product trends. The detection results, such as bounding boxes and confidence scores, were stored in the data warehouse for further analysis.

### 4. Data Exposure with FastAPI

To make the stored data accessible for analysis, **FastAPI** was implemented. This framework allowed us to expose APIs that provide access to the cleaned and enriched data from the data warehouse. The FastAPI endpoints were designed for CRUD operations (Create, Read, Update, Delete), enabling seamless data access for external applications.

## Conclusion

The data warehouse built for Ethiopian medical businesses integrates advanced scraping techniques, data transformation, object detection, and API exposure. This project provides Kara Solutions with a scalable system for storing and analyzing valuable business data, ensuring more informed decision-making.
