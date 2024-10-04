# Email Analysis Project
![Project Screenshot](https://raw.githubusercontent.com/username/repository/main/images/screenshot.png)
## Overview
This project performs an analysis of emails using Python, specifically focusing on sentiment analysis, visualizations, and summary statistics. The project begins with the extraction of email data from `.eml` files, followed by data transformation and loading into a structured format for analysis.

## Libraries Used
- **pandas**: For data manipulation and analysis.
- **seaborn**: For data visualization.
- **matplotlib**: For plotting graphs.
- **textblob**: For sentiment analysis.

## Dataset
The dataset is an Excel file named `email.xlsx` containing email details with the following columns:
- **Subject**: Subject of the email
- **From Email**: Sender's email address
- **To Email**: Recipient's email address
- **Date**: Date the email was sent
- **Time**: Time the email was sent
- **Body**: Content of the email
- **Attachments**: Indicates if there are attachments

### Sample Data
| Subject            | From Email                    | To Email                      | Date       | Time  | Body                                         | Attachments |
|--------------------|-------------------------------|-------------------------------|------------|-------|----------------------------------------------|-------------|
| Event Recap        | jane.smith@comdomain.com     | chris.wilson@comdomain.com   | 2024-09-25 | 08:51 | Dear chris.wilson, This is the body...     | Yes         |
| Weekly Report      | jane.smith@comdomain.com     | mark.jones@comdomain.com     | 2024-09-23 | 08:51 | Dear mark.jones, This is the body...       | Yes         |

## Data Extraction
Data is extracted from `.eml` files, transforming unstructured email data into a structured format for analysis.

## Data Cleaning
The dataset is cleaned to ensure it is free from null values and irrelevant characters. The newline characters in the body of the emails are replaced to facilitate better analysis.

## Data Visualization
- **Distribution of Emails by Sender**: A count plot is generated to visualize the number of emails sent by each sender.
  
- **Number of Emails Sent by Date**: A line chart is created to show the trend of emails sent over time.
  
- **Distribution of Email Body Lengths**: A histogram visualizes the distribution of email body lengths.

## Sentiment Analysis
Using the TextBlob library, the sentiment polarity of each email body is calculated. Emails are categorized into Positive, Negative, or Neutral based on their sentiment score.

### Sample Sentiment Data
| Body                                         | Sentiment | Sentiment Category |
|----------------------------------------------|-----------|--------------------|
| Dear chris.wilson, This is the body...     | 1.0       | Positive           |
| Dear mark.jones, This is the body...       | 1.0       | Positive           |


## Conclusion
This project provides insights into email communication patterns, including sentiment analysis, which can be beneficial for understanding the overall tone of the email interactions.

## Exporting Data
The cleaned and analyzed data is exported back to an Excel file named `email_data.xlsx` for further use or reporting.
