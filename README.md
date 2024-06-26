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

#### Solution:without CTE
![Screenshot 2024-04-30 222540](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/fe6e7d26-ee3b-4eed-a346-6ace381cb1c6)
![Screenshot 2024-04-30 222636](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/190343e8-65a3-4954-8d1f-6b5bdfc15d3a)

#### .............................................................................................................................................................................................................
                                             ## Created View:final_fact_events
![Screenshot 2024-04-30 234456](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/3f6fce61-9698-4724-a61c-a50002861aa7)
#### ...........................................................................................................................................................................................................


#### Q-4)Produce a report that calculates the Incremental Sold Quantity (ISU%) for each category during the Diwali campaign. Additionally, provide rankings for the categories based on their ISU%. The report will include three key fields: category, isu%, and rank order. This information will assistin assessing the category-wise success and impact of the Diwali campaign on incremental sales.
#### Note: ISU% (Incremental Sold Quantity Percentage) is calculated as the percentage increase/decrease in quantity sold (after promo) compared toquantity sold (before promo)

![Screenshot 2024-04-30 233808](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/bc2157ec-3c1b-4328-8c3e-87e604585576)
![Screenshot 2024-04-30 233827](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/66816da7-e146-4f1f-99e3-59338ffa5fe4)


#### Q-5)Create a report featuring the Top 5 products, ranked by Incremental Revenue Percentage (IR%), across all campaigns. The report will provide essential information including product name, category, and ir%. This analysis helps identify the most successful products in terms of incremental revenue across ourcampaigns, assisting in product optimization.

![Screenshot 2024-04-30 231935](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/34378c6f-13d3-409e-af54-b98892605769)
![Screenshot 2024-04-30 231951](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/7295e3d6-72ff-4fe2-92c2-1ed7e2e6a714)

_________________________________________________________________________________________________________________________________________________________________________________________________________________

Step 3 : Now, the database retail_events_db was loaded into Power Bi. The table that were included were: 

       1) dim_campaigns
       2)dim_products
       3)dim_stores
       4)final_fact_events(which was created in 'View')

Step 4 : Relationship was established between the fact table and the dimensions tables,inside the data model.       
![Screenshot 2024-05-01 083258](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/7eab1d9d-7206-4cb0-8456-f58db375a545)

Step 5:  Built measures shown below to analyse the performance in terms of 
1) Quantity sold before promotional offers were applied.
   
![Screenshot 2024-05-01 084515](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/bb6a0b2c-e7a3-40aa-bcb8-f2fee04464ab)

2)Quanity sold after  promotional offers were applied.

 ![Screenshot 2024-05-01 085516](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/ede03e35-5fe7-4836-aee9-8c7d22027f33)

3)Revenue before promotional offers were applied.(in Indian currency units such as Lakhs,crores,thousands)

Measure:
![Screenshot 2024-05-01 085817](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/9ab391eb-a11a-4c0a-816d-8f8f3e52870b)

Format:

![Screenshot 2024-05-01 085848](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/2def6229-744b-4a07-8f31-646b11ae0483)

4)Revenue after promotional offers were applied.(In Indian currency units such as Lakhs,crores,thousands)

Measure: 

![Screenshot 2024-05-01 092409](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/b5d7f346-bd4d-4953-832c-c39b2abf76b0)

Format: 

![Screenshot 2024-05-01 092224](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/1c593f0d-4660-49b3-9ea6-a2f6c122ad59)

5)Incremental Sold Unit(ISU)---(in Thousands,lakhs,crores)

Measure: 

![Screenshot 2024-05-01 093148](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/1675fefe-170e-4b77-a5bb-a34701e6cbf2)

Format: 

![Screenshot 2024-05-01 093159](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/706d89df-3237-4c38-9dbe-5dfd3079fa27)

6)Incremental Revenue(IR)

Measure:

![Screenshot 2024-05-01 093737](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/aa76ee42-407d-404f-b948-123dc0f20b3f)

Format:

![Screenshot 2024-05-01 093749](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/0a74569c-e2f7-4c7c-81ff-2029fdf48177)

7)% Increase in revenue(% IR)


![Screenshot 2024-05-01 094255](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/7780df9f-5ba1-4e86-8673-8bbf4b9bd8f2)

8)Store_count

![Screenshot 2024-05-01 095333](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/cb6273a7-cccc-43f6-b3a2-0b9519b3bd90)

9)Average Incremental Reveneu per Store

 ![Screenshot 2024-05-01 095619](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/6f4b44dd-41a8-4494-8031-600a6067ff9d)

 .............................................................................................................................................................................................
  ............................................................................................................................................................................................   
       Dashboard: Store Performance Analysis

![Screenshot 2024-05-01 100035](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/04e14b53-107d-4aec-8b82-ee9b516dae3f)


      Dashboard: Promotion Tye Analysis

![Screenshot 2024-05-01 100056](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/68665050-9130-46c0-920f-07ce9b00f7e7)


     Dashboard: Product and Category wise analysis

![Screenshot 2024-05-01 100109](https://github.com/Sidsharma11/Atliq_mart_sales_report/assets/167175484/269e3abc-2830-4cf3-af26-142aaf7a23d2)


