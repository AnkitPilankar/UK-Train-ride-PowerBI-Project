UK Train Ride Data Analysis Project 

Play with Dashboard : [https://app.powerbi.com/groups/me/reports/49d7d7c6-74d5-460b-a20d-aadec3dacf46/ReportSection?experience=power-bi](https://app.powerbi.com/groups/me/reports/49d7d7c6-74d5-460b-a20d-aadec3dacf46/ReportSection?experience=power-bi)

![eeee](https://github.com/user-attachments/assets/ce5aca1d-a1e1-47ce-b299-61da79d5c216)
![neww](https://github.com/user-attachments/assets/a9314cab-bb71-40d8-ae43-80d6cbc8fc35)






Challenge link :https://mavenanalytics.io/challenges/maven-rail-challenge/08941141-d23f-4cc9-93a3-4c25ed06e1c3

Overview:

This project analyzes UK Train Ride data sourced from Maven Analytics. The dataset contains approximately 31,000 records and 18 columns. The goal is to extract meaningful insights and visualize key metrics related to train performance, ticket sales, and delay reasons.

Dataset:

Source: Maven Analytics
Size: 31,000 records
Columns: 18
Key Metrics and Slicers
Slicers Created
Total Revenue
Total Tickets Booked
On-time Trains
Cancelled Trains
Delayed Trains
Refund Percentage
Average Ticket Price
Average Delay Time

Charts and Visualizations:
Most Frequent Train Routes,
Reason for Delay,
Total Transactions by Purchase Type,
Revenue by Ticket Type,
Tickets Booked by Payment Method,
Tickets Booked by Rail Card Type,
Heat Map to Show Correlation Between Date and Time,
Tooltip for Most Frequent Routes (Average Delay Time and Reason)

Matrix
Busiest Booking Time by Month,
Calculation Details,
Time Categorization,

To calculate and categorize time, the following steps were taken:
Extracting Hour from Time:
Extract the hour component from the time value (e.g., 1:30 becomes 1).

Categorizing Time:
Use a SWITCH function to categorize time into hourly segments.
Example: If the time is between 1 and 2, it falls into the "1-2" category.
DAX eg 
TimeCategory = SWITCH(
    TRUE(),
    [Hour] >= 1 && [Hour] < 2, "1-2",
    [Hour] >= 2 && [Hour] < 3, "2-3",
    [Hour] >= 3 && [Hour] < 4, "3-4",
    ...
    [Hour] >= 23 && [Hour] < 24, "23-24",
    "Other"
)
Project Features

Interactive Slicers: Allow users to filter data based on various metrics.

Insightful Charts: Visualize key aspects of the data including revenue, ticket bookings, delays, and reasons for delays.

Correlation Analysis: Use heat maps to explore the relationship between different variables.

Tooltips: Provide additional information on frequent routes, including average delay time and reasons for delays.

Matrix Visualization: Highlight the busiest booking times by month.

Conclusion
This project provides a comprehensive analysis of UK Train Ride data, offering valuable insights into train performance, ticket sales, and delays. The interactive visualizations and detailed metrics help in understanding the key factors affecting train operations and customer satisfaction.
