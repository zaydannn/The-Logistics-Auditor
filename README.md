# EXECUTIVE SUMMARY
From the results of my analysis, it was confirmed that, delivery delays is actually a primary factor of negative customer reviews which in turn mostly leads to customer churn with average reviews dropping from 4.29 to 3.46 for late deliveries, and from 4.29 to 1.78 for sper late deliveries.
Furthermore, beyond immediate feedback, these logistics failures significantly damage customer retention, as first-time customers who experience delays are far less likely to return.
This suggests that, delivery inefficiencies and ineffectiveness, actually affects brand reputation, customer retention which may in effect damage profitability.


# Link to streamlit dashboard
https://ml-project-gzj6bejrel6ylpcudvtmt2.streamlit.app/


# Data Cleaning Techniques
Removing Duplicates: The raw reviews dataset contained multiple reviews for some orders. I sorted these by the latest timestamp and kept only the most recent review for each unique order_id to ensure each customer's final sentiment and review was captured once.
Handling Incomplete Orders: Since the goal was to analyze actual delivery performance, I filtered out orders that did not have a recorded 'order_delivered_customer_date'. This removed "canceled" or "in-progress" orders that would have altered the delay calculations.
I created a new Days_Difference metric and a Delivery_Status categorical column. This turned raw timestamps into actionable labels like "On Time," "Late," and "Super Late" for the final visualization.
I also created a retention_% column to actally map how delays affect churn.
Standardizing Formats: I converted all date-related columns (estimated and actual delivery dates) into datetime objects. This allowed for precise mathematical calculations of the time delta between when a package was promised and when it arrived.



# Candidate's choice addition (Customer Retention vs Review/Sentiments)
I decided to opt for this because it is easily used for managerial decision making. We can visually see the rate at which new customers leave or stay depending on the delivery time of their package.
This analysis evaluates how first delivery experience affects customer retention. Customers whose first order was delivered on time are compared against those who experienced delays. The retention rate is calculated as the percentage of customers who returned to make another purchase. The results help determine whether delivery performance influences long-term customer loyalty.

# Powerpint Link
https://1drv.ms/p/c/98d0db72bd603a77/IQDycs7kKiRpSJeZrlItZ5UGARhZ1x3AT3QFS1B5cfH7XlY?e=Erewt2
