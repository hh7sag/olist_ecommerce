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
