Data Modelling Power BI

This is a US Butter data modelling:

I started this project from a news articles: 
- https://vespertool.com/news/us-butter-prices-drop-sharply-on-cme-as-abundant-milk-supply-weighs-on-dairy-markets/
- https://www.latimes.com/business/story/2025-09-17/americas-butter-glut-is-driving-prices-to-three-year-lows

Based on these articles:
- I tried to understand the trend of butter production and price in US
- Also how other factors like milk price, milk fat content, milk production, dairy herd count is potentially affecting butter

This project is still in progress as I continue collecting and adding more data.

I have 3 FACT Tables
- Milk Production and Wholesale Price (clal milk)
- Butter production (nass butter)
- Butter Wholesale Price (clal wholesale_price)

I modelled the data in Power BI by creating the following DIMENSION tables:
- Dim_Country
- Dim_Date
- Dim_Measure
- Dim_Product

There exists One to Many relationship between Dimension Tables and Fact Tables. Please see the snapshot of the data modelling below for better understanding
<img width="1135" height="737" alt="image" src="https://github.com/user-attachments/assets/03f782e6-14a2-485e-afb9-bc468d77bf1e" />

<img width="1001" height="752" alt="image" src="https://github.com/user-attachments/assets/b2013f13-4420-4dd0-ae3a-fa445e13a819" />

<img width="1037" height="658" alt="image" src="https://github.com/user-attachments/assets/13fef14b-f046-4356-9034-2ddca2d4999b" />

Source Reference:
USDA,
Vesper,
clal,
News Articles
