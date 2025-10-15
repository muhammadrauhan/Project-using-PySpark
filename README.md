# Cleaning an E-Commerce Orders Dataset with PySpark
<div align="center">
    <img width="1224" height="346" alt="data check" src="https://github.com/user-attachments/assets/6054c8b8-7f04-447c-9fa7-31e91ef0bd12" />
</div>

## :bulb: About
In this project, I had stepped into a role of a data engineer at an E-Commerce company and use PySpark, a powerful tool for data processing. I have been requested by a peer Machine Learning team to clean the data containing the information about orders made last year. They are planning to further use this cleaned data to build a demand forecasting model. To achieve this, they have shared their requirements regarding the desired output table format.

An analyst shared a parquet file called `orders_data.parquet` for you to clean and preprocess.

You can see the dataset schema below along with the cleaning requirements:

<div align="center">
    <img width="745" height="400" alt="data" src="https://github.com/user-attachments/assets/3f06c77a-f7c5-4b26-a59f-2ccdf4ccd855" />
</div>

## :jigsaw: Project Approach
My step-by-step approach throughout the project was:
+ Read and load the raw orders data.
+ Processed and standardized the order date column.
+ Cleaned product information columns for consistency.
+ Extracted state details from addresses and counted unique states.
+ Prepared and exported the final cleaned dataset for analysis.

- ### Load the Parquet File to PySpark DataFrame:

  <div align="center">
      <img width="744" height="290" alt="data-head" src="https://github.com/user-attachments/assets/54adef6c-3701-4aba-873d-f51ccd77cedb" />
  </div>

  Here you can see that the total count for `orders_data.parquet` is **185,950** records, before any transformation is done.

- ### Dealing with `order_date` Column:

  Created a `time_of_day` column.

  <div align="center">
      <img width="744" height="301" alt="column" src="https://github.com/user-attachments/assets/61ceae12-53e7-4669-9e9d-f912cd1de5c1" />
  </div>

  - #### Removed the rows containing an Orders made at Night Time:

    <div align="center">
        <img width="750" height="79" alt="rem-row" src="https://github.com/user-attachments/assets/b2a1faa6-9a70-4919-add0-6332ec5bef14" />
    </div>

    Here you can clearly see that the total count is **176,762** records, after removing the rows containing an orders made at night time.
    <br>
    <br>
    <br>
    
  
If you want to see my further cleaning, transformation and data processing approach you can see my `.py` file here [Data Processing File](https://github.com/muhammadrauhan/Project-using-PySpark/blob/main/data-cleaning-and-processing.ipynb).
<br>
<br>
<br>
<br>
<br>

> [!NOTE]
> I completed this project from **DataCamp**, If you want to do this project you can visit the site by clicking on this [DataCamp PySpark Project](https://app.datacamp.com/learn/projects/2355).


    
