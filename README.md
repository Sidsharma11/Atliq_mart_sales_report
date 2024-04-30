# AltiQ Mart Festival Sales Analysis

### Dashboard Link : https://app.powerbi.com/groups/me/reports/7c18ac08-a8fb-40f0-aa57-9c52b304324b/ReportSectionba4ff280bf4746008189?experience=power-bi

## Problem Statment
AtliQ Mart is a retail giant with over 50 supermarkets in the southern region of India. All
their 50 stores ran a massive promotion during the Diwali 2023 and Sankranti 2024
(festive time in India) on their AtliQ branded products. Now the sales director wants to
understand which promotions did well and which did not so that they can make
informed decisions for their next promotional period.

The dashboard is designed to provide an overview of the various discounts offered and their impact on sales.

### Steps followed:

Step 1 : Imported the 'retail_events_db' database into MySQL Workbench. 

Step 2 : Crafted SQL queries to address the specified business questions given below:

#### Q-1) Provide a list of products with a base price greater than 500 and that are featured in promo type of 'BOGOF' (Buy One Get One Free). This information will help us identify high-value products that are currently being heavily discounted, which can be useful for evaluating our pricing and promotion strategies.


   ![Screenshot 2024-04-30 181441](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/afe9c9bc-7136-45c6-b61c-ef93fa3701e8)

#### Q-2)Generate a report that provides an overview of the number of stores in each city.The results will be sorted in descending order of store counts, allowing us toidentify the cities with the highest store presence.The report includes two essential fields: city and store count, which will assist in optimizing our retail operations.

![Screenshot 2024-04-30 191311](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/0c29d0d6-abce-4e1b-ad38-26494fa44c50)

#### Q-3) Generate a report that displays each campaign along with the total revenue generated before and after the campaign? The reportincludes three key fields: campaign_name, total_revenue(before_promotion), total_revenue(after_promotion). This report should help in evaluating the financialimpact of our promotional campaigns. (Display the values in millions)

#### Solution:Using CTE
![Screenshot 2024-04-30 221652](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/fe7b3876-a7ed-46fc-875f-0cb8d8630b2d)
![Screenshot 2024-04-30 221940](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/5f01b6e9-363b-41d7-84da-0733df9786cf)


