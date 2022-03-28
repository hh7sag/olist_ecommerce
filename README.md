# Olist_ecommerce
Olist ecommerce is a project which I focused on analyzing product change in space and time across Brazil

![image](https://user-images.githubusercontent.com/97778235/160345575-4484b27a-8e42-46dd-9ef0-73e5a1a6b1e5.png)

## Overview
For Olist projects, there are 8 datasets in total, but I only use 2 datasets including customers dataset and products datasets to analyze product changes based on total number of orders (key metric) and successful orders (supporting metric)

+ Customer dataset: It has 99441 customers with 5 columns of ID, unique_ID, zip_code_prefix, city and states in Brazil

![image](https://user-images.githubusercontent.com/97778235/160346724-41691656-7587-4f54-bf41-ca0e3fcf59e1.png)

+ Product dataset: It has 32951 products with nearly 73 product categories and other product features such as photo quantity, name length, description length, weight, length, width and height

![image](https://user-images.githubusercontent.com/97778235/160347515-17d57eac-767f-4c93-9d29-d370c1ff2382.png)

Then, calculating the product volume by multiplying the length * width * height of the products

![image](https://user-images.githubusercontent.com/97778235/160348904-a0d0f4f4-96ad-4e9c-99f1-49cea34c17a9.png)

![image](https://user-images.githubusercontent.com/97778235/160348991-b7ad35d1-d88c-47c4-9ef3-3eace6741879.png)

## Problem Statement
Imagining that you are a consultant, and your customer is founder of Olist. The customers need some insights to have a better view of product classification through regions and timeline. Based on 2 ways of regions (space) and timeline (time), you are required to make an analysis.

## Methodology 
### Cleaning the data

Firstly, I divide the customer states into 5 regions including North, North East, Mid Central, South and South East as the following map

![image](https://user-images.githubusercontent.com/97778235/160351449-a7e7abd5-e78b-49b2-bec8-651cc604f023.png)

Filtering out 73 product categories into 26 product categories and creating a new column name 'category_2' since the original product categories are poorly classified. For example, fashion_accessories, fashion_men, fashion_women are seperted and combined into 1 product category "fashion"

![image](https://user-images.githubusercontent.com/97778235/160353446-4c510def-2663-421f-84b6-9d4e09792ae2.png)

Then, merge the product with customer, pcn_trans (product translations) and order items into 1 final table and converted the date into periods (month/year)

![image](https://user-images.githubusercontent.com/97778235/160353778-3ac0138b-0702-42c7-b98d-750ac01d5a23.png)

### Exploratory Data Analysis
#### Simple EDA  

As mentioned, there are 2 main criteria to choose top product categories: total number of orders and total sucessful orders as key metric and supporting metric.
In terms of total number of orders, there are the top 5 categories with highest number of orders, with home office furniture and bed bath table top the chart

![image](https://user-images.githubusercontent.com/97778235/160361253-0757b252-fde0-47e0-97a3-61b990f80f64.png)

Then, I analyze the top 5 categories from time to time to get the overview of the trend. From the line chart, the number of orders gradually increased.

![image](https://user-images.githubusercontent.com/97778235/160362140-fa643d6c-a499-4d69-a9c2-f4973138cf23.png)

It can be demonstrated from the graph that the number of orders in 5 categories started at Sep/2016 and continued going up and down until reaching their peaks in Nov/2017 (maybe BlackFriday demand). Also, there were some ongoing trends such as health_beauty products after reaching its 1st peak in Nov/2017, it continued to go up in 2018 and sudden increase in computer_games rising up in Feb/2018. After the 1st peak in Nov/2017, bed bath table, sports leisure and home office furniture slowly went down

Regarding successful orders, we filter the orders using order status as delivered. Then, counting number of successful orders and choosing the top5 product categories as follow:

![image](https://user-images.githubusercontent.com/97778235/160364460-522a0b9e-09ed-4e4d-9949-88a65b5dbed9.png)

In the top 5 categories mentioned in the bar graph, home office furniture and bed_bad_table products all have the highest number of successful orders

Like total number of orders, I also analyze the trend over the last 2 years as follow:

![image](https://user-images.githubusercontent.com/97778235/160368898-9c1e50d8-c833-41f9-a5ea-d4068ec78808.png)

It can be demonstrated from the chart that the total successful orders in 5 categories started at Oct/2016 and continued going up and down until reaching their peaks in Nov/2017 (maybe BlackFriday demand). Their patterns kept increasing but the pace were unstable. 

After analysizing based on total price, total number of orders and total successful orders, it is clearly stated from most of the charts that Nov/2017 witnessed the sudden rise in categories such as bed_bath_table, health_beauty, computer games and home office furniture. 


