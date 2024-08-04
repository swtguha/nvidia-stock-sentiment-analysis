**NVIDIA Market Analysis and Sentiment Analysis**
This project integrates stock market analysis for NVIDIA (NVDA) with sentiment analysis of Reddit posts related to NVIDIA. It uses Alpha Vantage for obtaining stock data and FinBERT for analyzing the sentiment of Reddit posts. Data fetching from Reddit is handled asynchronously to improve efficiency.

**Features**
**Stock Market Analysis:** 
Retrieves historical and real-time stock data for NVIDIA using the Alpha Vantage API. This data provides insights into market trends and trading activities.
**Sentiment Analysis:** Analyzes the sentiment of Reddit posts mentioning NVIDIA using FinBERT, a sentiment analysis model tailored for financial text. The sentiment analysis helps understand public perception and market sentiment around NVIDIA.
Asynchronous Data Fetching: Utilizes asyncpraw for asynchronous retrieval of Reddit posts. This method improves the efficiency of data collection by allowing multiple requests to be processed concurrently.
**Error Handling:** Implements robust mechanisms to handle errors, including rate limits and network issues, ensuring reliable data retrieval and processing.
Setup
**Install Dependencies:** Install required Python libraries such as asyncpraw, aiohttp, transformers, pandas, matplotlib, seaborn, and alpha_vantage.

**Obtain API Credentials:**

Reddit API: Created a script application on Reddit to get client_id, client_secret, and user_agent. Replace placeholders in the script with these credentials.
Alpha Vantage API: Register on Alpha Vantage to get an API key for accessing stock data. Use this key in your script to fetch stock information.
FinBERT Model: FinBERT is a pre-trained sentiment analysis model that specializes in financial texts. It is used to analyze the sentiment of Reddit posts related to NVIDIA.

**How It Works**
**Stock Data Retrieval:** The script connects to Alpha Vantage to fetch intraday stock data for NVIDIA. This data includes high-frequency trading information, which is valuable for market analysis.

**Reddit Data Retrieval:** Using asyncpraw, the script asynchronously fetches Reddit posts mentioning NVIDIA. This approach enables efficient handling of large volumes of data.

**Sentiment Analysis:** The FinBERT model processes the fetched Reddit posts to determine their sentiment. It classifies posts as positive, negative, or neutral, providing insights into public opinion about NVIDIA.

**Error Handling: The script is designed to handle various issues:**

**Network Issues:** Implements retries with exponential backoff to address temporary network errors.
**Rate Limits:** Manages rate limits by pausing and retrying requests when necessary.
**Data Quality:** Includes checks to ensure the consistency and reliability of the retrieved data.
**Contributing**
Contributions to enhance the functionality or improve the project are welcome. Please open issues or submit pull requests with any changes or enhancements.

**License**
This project is licensed under the MIT License.

