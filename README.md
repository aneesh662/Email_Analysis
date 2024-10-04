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

