# ETL_steam_top_100

Members: Christi Bragg, Lowell Vaughen and Joseph Pegram

Modules:

    Browser
    Beautiful Soup
    Pandas
    Pymongo
    Requests

**E**xtract

Sources of Data:


    Kaggle - https://www.kaggle.com/varunsaha/mygamedataset?select=steam_games.csv
        CSV: steam_games.csv
    Steam Scrape URL: 'https://store.steampowered.com/stats'
        Jupyter Notebook: steam_self_changed.ipynb

    The first obstacle to overcome was extracting the data from Steam. Modules Browser and Beautiful Soup were used to scrape the data off of the Steam website and used click to find the top 100 games.

**T**ransformation

The dataset was inserted into a Pandas Dataframe.

    Transformation Required:
    DropNa of the blank rows.
    The column headers (current players and Peak today) was split and separated
    Rename the column headers
    Concatenate the Player Data to Game Name
    Stripped the leading space from the Game column
    Joined/Merged the Dataset
    
    CSV: steam_final_df.csv

**L**oad

    The final datebase was loaded into MongoDB.


Challenge:

    The dataset was not fully complete, due to some of the games not being released or updated when the data was scraped from the Kaggle csv, so in order to complete the dataset additional data was manuallly inserted into the dataset.
