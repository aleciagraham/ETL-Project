**Summary of ETL project:**

This ETL project was to take in a CSV and Transform, analysis and Load into a Postgres Database.

We chose a CSV of Cars and a CSV of Fuel that would allow us to analyze the electric vehicles technology growth through the years and to project when the best year would be to purchase an electric cars (based on the greatest Benefit-Cost Ratio). 

To achieve this we pulled both CSVs into Juptyer notebooks for data cleansing.

​	The process for the CSV of Cars (FEWS.csv), was to read it into a Jupyter Notebook, Review the column names and their order. Utilize the CSV documentation from the source to decipher the names of the columns. Renamed them to friendly names and dropped unneeded columns. Reordered the columns. Filtered by date. Reformatted dtypes. Write to a CSV

![image-20200902161455416](images\image-20200902161455416.png)

​	The process for the CSV of Fuel (two separate CSVs). Read both CSVs into a Jupyter Notebook. Reformat the date columns to be able to merge based on year only.  Filtered by date. Merged the two CSV sources to create a single fuel DataFrame on the Year column. Removed the '$' symbol and replaced it with nothing. Changed the data type of an object to a float for the cost of fuel. Write to a CSV

![image-20200902162147581](images\image-20200902161349215.png)

​	When both of these processes were complete, read into a different Jupyter Notebook, which utilized a create_engine that created the CSVs as tables into Postgres Database.



#This is the mode we used to load it.

![image-20200902161946305](images\image-20200902161946305.png)