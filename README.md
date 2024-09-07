# Travel Agency Customer Data Analysis

### Project Objective

This  project aims to create an interactive data dashboard that provides comprehensive insights into the travel patterns, customer demographics, financial performance, and booking trends for a travel agency. The goal is to utilize this dashboard to enhance decision-making processes, optimize marketing strategies, improve customer satisfaction, and ultimately increase the agency's revenue.

### Tools Used

- Data Analysis and Visualization: Microsoft Excel
- Dashboard Development: Microsoft Excel

### Data Description

The primary dataset used for this analysis is the "Travel.xlsx" file containing detailed information on customers, their bookings, package details, and customer feedback. The dataset contained 10,000 rows and included the following columns:

- Customer_ID: A unique identifier for each customer.
- Customer_Name: The name of the customer.
- Age: The age of the customer.
- Age-group: The age-group of customers, e.g., "15-29", "30-44", etc.
- Gender: The gender of the customer, i.e., "Male" or "Female".
- Income_Level: The income level of the customer, categorized as "Low," "Medium," or "High."
- Destination: The travel destination chosen by the customer.
- Continent: The continent where the travel destination is located. 
- Climate_Info: Information about the climate of the chosen destination, providing insights into the weather conditions.
- Package_Price: The price of the travel package.
- Real Package_Price: The price paid by customers, i.e., after discount has been applied.
- Discount: Any applicable discount percentage on the package price.
- Revenue: Th revenue generated per booking date.
- Booking_Date: The date on which the customer made the booking, containing dates between 2008 (the agency's start year) and 2023.
- Cancellation_Rate: The rate of booking cancellations, ranging from 0% and 20%.
- Customer_Feedback: Feedback or review provided by the customer about their travel experience.
- Customer_Rating: Ratings based on customer's feedback on their travel experience.
- Season: The season in which the travel took place, i.e., "Spring", "Summer", "Fall", or "Winter".
- Holiday_Info: Information about the type of holiday, e.g., "Summer Sunshine", “Easter Escape", etc.
- Is_Returning_Customer: indicates whether the customer is a returning customer of the agency ("true" for returning customers or "false" for one-time customers).

### Data Cleaning and Preparation
The dataset underwent thorough cleaning and preparation to ensure data integrity and suitability for analysis. Below are the approach taken:

- creating a table using CTRL + T,
- standardizing formats,
- creating new columns:
   - Age-group, using (=IF([@Age] <= 29, "15-29", IF([@Age] <= 44, "30-44", IF([@Age] <= 59, "45-59", "60+")))).
   - Real Package_Price, using (=[@[Package_Price]]-([@[Discount(%)]]%*[@[Package_Price]])).
   - Revenue, using (=SUMIFS([Real_Package_Price], [Booking_Date], Q2)).
   - Customer_Rating, using (=IF([@[Customer_Feedback]]="Wonderful trip, highly recommended.", 5, IF([@[Customer_Feedback]]="Great experience overall!", 2, IF([@[Customer_Feedback]]="Will definitely come back.", 4, IF([@[Customer_Feedback]]="Could be better.", 1, 3))))).
    - Continent, using (=SWITCH([@Destination],"Australia","Australia","Spain","Europe","Saudi Arabia","Asia","Dubai","Asia","Kenya","Africa","South Africa","Africa","China","Asia","Japan","Asia","South Korea","Asia","Rwanda","Africa","Nigeria","Africa","Egypt","Africa","Canada","North America","Thailand","Asia","New York","North America","Italy","Europe","France","Europe")).


### Exploratory Data Analysis (EDA)

EDA was conducted using pivot tables and statistical techniques to understand the key patterns and uncover insights into customer demographics and behaviors, and financial performance of the travel agency. Demographic analysis revealed customer profiles, while booking trends, seasonal analysis, holiday information, financial performance, discount impact, top destinations, continent analysis, customer ratings, cancellation rates and climate preferences were analyzed across the years(2008-2023).

This EDA provides the foundation for building a comprehensive and insightful dashboard. The key findings will help in shaping the visualizations and interactive elements, ensuring that the dashboard meets the travel agency's needs for data-driven decision-making.


### Results and Insights

1. 
