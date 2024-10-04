# Email Analysis Project

## Overview
This project performs an analysis of emails using Python, specifically focusing on sentiment analysis, visualizations, and summary statistics.

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

## Analysis Steps

1. **Load Data**: Import the Excel file into a pandas DataFrame.
   ```python
   import pandas as pd
   email_df = pd.read_excel("email.xlsx")
#Data Exploration
email_df.head()
email_df.info()
email_df.describe()

#Data Cleaning:
email_df['Body'] = email_df['Body'].replace('\n', ' ', regex=True)

#Visualizations:
import seaborn as sns
import matplotlib.pyplot as plt

sns.countplot(data=email_df, x='From Email')
plt.show()


#Sentiment Analysis: 
from textblob import TextBlob

def get_sentiment(text):
    return TextBlob(text).sentiment.polarity

#Group Data

email_df['Sentiment'] = email_df['Body'].apply(get_sentiment)
email_df['Sentiment Category'] = email_df['Sentiment'].apply(lambda x: 'Positive' if x > 0 else ('Negative' if x < 0 else 'Neutral'))

email_df[['Username', 'Domain']] = email_df['To Email'].str.split('@', expand=True)
to_name = email_df.groupby('Username')['Domain'].count()


#Export Results:
email_df.to_excel('email_data.xlsx', index=False)