# Data_Cleaning_using_SQL
Recently, I worked on cleaning a real dataset about employee layoffs using SQL.
Here’s the process I followed to make the data ready for analysis 

1️⃣ Remove Duplicates
I used ROW_NUMBER() with a CTE to identify and delete duplicate rows, keeping only the unique records.

2️⃣ Standardize the Data

Applied TRIM() to remove extra spaces.

Unified similar industry names like “crypto” that appeared in multiple forms.

Converted text dates into proper DATE format using STR_TO_DATE().

Cleaned country names by removing unnecessary punctuation (e.g., trailing dots after “United States”).

3️⃣ Handle Null or Blank Values

Replaced empty strings ('') with NULL.

Used JOIN statements to fill missing values based on other rows with the same company.

Deleted rows that didn’t contain any useful information (like when both total_laid_off and percentage_laid_off were NULL).

4️⃣ Drop Unnecessary Columns
Finally, I removed helper columns like row_num that were only used during the cleaning process.
