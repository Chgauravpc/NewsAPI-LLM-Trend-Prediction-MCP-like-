# News Analysis Script

This repository contains a Python script (`live_trend_analysis.py`) that fetches and analyzes news articles using the NewsAPI and Together AI API. The script retrieves news articles based on a user-specified topic, fetches the full content using Jina Reader, and analyzes the content for factors like sentiment, stock market impact, and economic indicators, returning results in a structured JSON format.

## Purpose and Context

The script is a standalone tool for analyzing news articles but can be considered a **mock implementation of an MCP (Master Control Program)-like server** by simulating centralized data processing. Below, we explain how it emulates an MCP server.

### How This Script Mocks an MCP Server

An MCP server, inspired by a centralized control system, aggregates and processes data to provide structured outputs. This script mimics this in the following ways:

1. **Data Aggregation**: Fetches news articles from NewsAPI and full content via Jina Reader, acting as a central data collector.
2. **Data Analysis**: Uses Together AI’s Llama model to analyze articles for sentiment, emotion, stock market effects, and economic indicators, mirroring a server’s data-processing role.
3. **Structured Output**: Returns analysis in JSON format, similar to a server’s response to clients.
   ```json
   {
       "Overall_Sentiment": "Neutral",
       "Emotion_Detection": "Optimism",
       "Polarity_Score": 0.2,
       "Stock_Market_Effect": "No significant impact",
       "Search_Volume": "Medium",
       "Revenue_Profit_Impact": "Stable",
       "Recession_Signals": "None",
       "Supply_Demand_Gaps": "None",
       "Employment_Opportunity": "Stable"
   }
   ```
4. **Workflow Simulation**: Executes a pipeline (input topic → fetch articles → analyze → output), resembling a server’s request-processing workflow.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/news-analysis-script.git
   cd news-analysis-script
   ```

2. Install dependencies:
   ```bash
   pip install requests together
   ```

3. Set up API keys:
   - Obtain a NewsAPI key from [newsapi.org](https://newsapi.org).
   - Obtain a Together AI API key from [together.ai](https://together.ai).
   - Update the `NEWS_API_KEY` and `TOGETHER_API_KEY` variables in `live_trend_analysis.py` with your keys.

## Usage

Run the script and enter a news topic when prompted:
```bash
python live_trend_analysis.py
```
Example:
```
Enter the news topic you want to search for: technology
```

The script will fetch up to five articles, analyze them, and print the results in JSON format.

## Dependencies

- Python 3.6+
- `requests`: For making HTTP requests to NewsAPI and Jina Reader.
- `together`: For interacting with the Together AI API.
- External APIs:
  - NewsAPI (for fetching news articles)
  - Jina Reader (for fetching full article content)
  - Together AI (for article analysis)

## File Structure

- `live_trend_analysis.py`: Main script for fetching and analyzing news articles.
- `README.md`: This file, providing project overview and instructions.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for bug fixes, enhancements, or new features. To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
