# twitter-x-data-extraction


## Overview
This project utilizes Selenium to scrape real-time tweets from Twitter based on user-defined hashtags and post count. It automates the process of logging into Twitter, searching for tweets, and extracting relevant details such as tweet content, username, date, engagement metrics, and media links.

## Features
- **Automated Twitter Login** (requires manual input for login credentials initially)
- **Hashtag-based Tweet Scraping**
- **Extracts Engagement Metrics** (likes, retweets, replies, views)
- **Extracts Tweet Media** (images and hashtags)
- **Saves Data to CSV for Analysis**

## Prerequisites
- Python 3.x
- Google Chrome installed
- ChromeDriver (compatible with your Chrome version)
- Required Python libraries:
  ```sh
  pip install selenium pandas
  ```

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```
2. Download and place `chromedriver.exe` in a known location.
3. Update the `driver_path` in the script:
   ```python
   driver_path = r"C:\Users\New\Downloads\chromedriver-win64\chromedriver.exe"
   ```

## Usage
1. Run the script:
   ```sh
   python twitter_scraper.py
   ```
2. Manually log in to Twitter when prompted.
3. Enter the hashtag (including `#`) and the maximum number of tweets to scrape.
4. The script will scroll and extract tweets until the specified count is reached.
5. Extracted tweets will be saved to a CSV file named `{hashtag}_tweets.csv`.

## Output Data
The extracted CSV contains the following columns:
- `user_posted`: Twitter handle of the user
- `date_posted`: Timestamp of the tweet
- `description`: Tweet text
- `views`: Number of views
- `replies`: Number of replies
- `reposts`: Number of retweets
- `likes`: Number of likes
- `hashtags`: Hashtags used in the tweet
- `is_verified`: Whether the account is verified
- `photos`: Links to images in the tweet
- `url`: Source URL

## Notes
- This script requires manual login for authentication.
- Twitter may block scraping activity if excessive requests are made. Consider using time delays and a headless browser mode.

## License
This project is licensed under the MIT License. Feel free to modify and distribute it.

## Contact
For any issues or suggestions, please create an issue or contact me at [dhaaranipushpam@gmail.com].

