## The goal of this project was to learn how to create a relational database in AWS, import a dataset and query the data.

## Steps taken:

- Created a **relational database** using **AWS RDS**
- Created a **data table** with **postgreSQL pgAdmin**
- **Imported Seattle Rain History dataset** from Kaggle (https://www.kaggle.com/datasets/rtatman/did-it-rain-in-seattle-19482017)
- **Connected to my database** using **DataGrip**
- **Using SQL**, analyzed the **top 10 avg. years** of precipitation in Seattle, WA

## Here's what it looks like...

## Querying the **top 10 avg. years of precipitation (in inches) in Seattle, WA** using DataGrip:

<img src="https://user-images.githubusercontent.com/93350017/167045246-87af31d8-4200-4200-bca4-b37e2450e5a0.png" width="500">

## What am I doing here?

- I created a **CTE** and used **dense_rank()** over the **rounded average precipation per year**. 

- I **rounded the avg. precipiation** by 6 decimal places because the original dataset included more decimals than I required. 

- I used **dense_rank** because I wanted to **include any potential duplicate results**, although that would not likely occur in this scenario.

- I **ordered the ranking by the average precipiation in descending order**, to start with the highest amount of precipitation to the lowest.

- I **grouped the results by year** using the **extract function**.

- I selected the **avg_prcp, year and ranking columns** from my CTE and only included the results that were less than or equal to a rank of 10.


## Using pgAdmin to create a table and import data:

<img src="https://user-images.githubusercontent.com/93350017/167046224-9b33a905-5557-4e8c-87e1-72bc64818c77.png" width="1300">

## Creating a postgreSQL relational database using AWS RDS:

<img src="https://user-images.githubusercontent.com/93350017/167046668-52e6a013-29e0-42b9-b65c-c289bfcc9a40.png" width="1300">
