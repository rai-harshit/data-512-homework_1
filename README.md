## Project Goal

The objective of this project is to track, from 2015 to 2023, the pageview traffic of a sample of Wikipedia articles pertaining to Academy Award-winning films. The research seeks to produce three unique datasets: monthly access from mobile devices, monthly access from desktop computers, and monthly cumulative pageviews.

## Data Sources

- **Wikipedia Pageviews Data**: This project relies on the Wikimedia Foundation REST API to access pageview data for Wikipedia articles. The data spans from July 2015 through the previous complete month.

## Data Processing and Analysis

Data collection, data processing, and dataset development are some of the major processes in the project:

1. **Data Acquisition**: The project retrieves pageview counts for particular Wikipedia articles using the Pageviews API.

2. **Data Processing**: The retrieved data is grouped into time series representing monthly pageview activity after being processed.

3. **Dataset Creation**: There are three datasets produced:
   - Monthly Mobile Access: Pageviews from mobile apps and mobile web combined.
   - Monthly Desktop Access: Desktop pageviews.
   - Monthly Cumulative: The total of each article's desktop and mobile traffic.

## Documentation

The project follows the recommended procedures for replication and documentation:

- Jupyter Notebook(s): Detailed explanations of the steps involved in data collection, processing, and analysis.

- README File (this file): Gives a general description of the project, outlining its objectives, data sources, data processing procedures, and reproducibility standards.

- LICENSE File: This file contains the code's MIT LICENSE, which guarantees that it can be used freely.

## License

This project is open-source and follows the MIT License. You are free to use and modify the code following the terms of the MIT License.

## API Documentation

- **Wikimedia Foundation REST API**: This project uses the Wikimedia Foundation REST API to access pageview data. For API documentation and terms of use, please visit: [Wikimedia Foundation REST API Documentation](https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions)

## Known Issues

- One article (Victor/Victoria) returning 404 API response, meaning the URL is not found.
- Please contact the data owner listed in the source if you have any problems with a particular API related to any of the articles.

## Output Files

- The project generates three JSON files:
  - `academy_monthly_mobile_201507-202312.json`: Monthly mobile access data.
  - `academy_monthly_desktop_201507-202312.json`: Monthly desktop access data.
  - `academy_monthly_cumulative_201507-202312.json`: Monthly cumulative data.

Please refer to each file for detailed data on Wikipedia pageviews.

## Analysis Steps

1. Data collection: Python code was used to get data from the Pageviews API.
2. Data processing: To determine average pageviews, identify articles with the highest and lowest pageview totals, and locate articles with the fewest months of data, the obtained data was processed.
3. Data Visualization: To display the findings of the investigation, three graphs were made:
   - Maximum and Minimum Average Page Requests
   - Top 10 Peak Page Views
   - Articles with Fewest Months of Data
4. Interpretation: To glean insights from the data, the analysis's findings were interpreted.

## Reproducing the Analysis

To reproduce this analysis, you can perform the following steps:

1. Clone this repository to your local machine
2. Verify that Python is installed and that the necessary libraries (pandas, matplotlib, json, requests, tqdm) are installed
3. Run data_acquisition.ipynb in Jupyter Notebook to create all the necessary JSONs
4. Use data_visualization.ipynb from Jupyter Notebook to create all of the graphs, which will be saved in the parent folder
5. Examine charts

**Note**: For additional details and code implementation, please refer to the provided Jupyter Notebook(s).
