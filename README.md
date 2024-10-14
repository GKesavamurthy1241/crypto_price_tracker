# crypto_price_tracker

This project contains scripts and a database for fetching and storing cryptocurrency prices. It includes the following components:

# Project Structure

crypto_prices.db: SQLite database file that stores cryptocurrency price data.
db_setup.py: Script for setting up the database schema.
fetch_and_store.py: Script for fetching cryptocurrency prices from an API and storing them in the database.

#  Requirements

Python 3.x
SQLite3

#Required libraries:

requests (for API calls)
sqlite3 (for database interaction)

# Usage

# 1. Setting Up the Database

Before fetching and storing data, you need to set up the database schema. Run the db_setup.py.This will create the necessary tables in crypto_prices.db to store the cryptocurrency price data.

# 2. Fetching and Storing Cryptocurrency Prices

After setting up the database, you can fetch and store the cryptocurrency prices using fetch_and_store.py. This script fetches price data from an API and inserts it into the database.The script can be scheduled to run at regular intervals (e.g., using a cron job) to keep the database up-to-date with the latest price data.

# Database Schema

The crypto_prices.db database contains the following table:

# prices:

id (INTEGER PRIMARY KEY): Unique identifier for each entry.
currency (TEXT): The name of the cryptocurrency.
price (REAL): The current price of the cryptocurrency.
timestamp (TEXT): The time at which the price was fetched.

# Customization

API Source: The API used to fetch cryptocurrency prices can be modified in the fetch_and_store.py script. Update the API URL and parameters according to the API provider's documentation.
Database Path: If you wish to change the location of the database, update the path in both db_setup.py and fetch_and_store.py.
