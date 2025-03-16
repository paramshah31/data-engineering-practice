## Exercise 7 - Using Various PySpark Functions
In this exercise we are going to have some problems to solve that will require us to use various PySpark functions. You should only use functions provided in `spark.sql.functions`. Do not use UDF's or Python methods to solve the problems! We will be using open source hard-drive failure data files as our source data.

### Tasks:
1. Add the file name as a column to the DataFrame and call it `source_file`.
2. Pull the date located inside the string of the `source_file` column. Final data-type must be date or timestamp, not a string. Call the new column `file_date`.
3. Add a new column called `brand`. It will be based on the column `model`. If the column model has a space ... aka   in it, split on that space. The value found before the space will be considered the brand. If there is no space to split on, fill in a value called `unknown` for the brand.
4. Inspect a column called `capacity_bytes`. Create a secondary DataFrame that relates capacity_bytes to the model column, create "buckets" / "rankings" for those models with the most capacity to the least. Bring back that data as a column called `storage_ranking` into the main dataset.
5. Create a column called `primary_key` that is `hash` of columns that make a record unique in this dataset.
