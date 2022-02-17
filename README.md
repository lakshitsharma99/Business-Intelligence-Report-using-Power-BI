# Business-Intelligence-Report-using-<a href="https://lakshitsharma99.github.io/powerbi.html">Power-BI</a>

# Business / Functional Requirement Document

# 1. Data Gathering / Requirement:
Assemble a sales reports with different visuals to best show the Sales Insights in one page Dashboard. Feel free to use your imagination to best represent the data you have available.

* Sales (folder by year)
* Categories (Excel)
* Geography (Excel)
* Product (CSV)
* SalesRep (Excel)
* SubCategories (Excel)

<b>Task 1.1</b>:<br>
Create a mechanism to load all the files from the sales folder in a single Sales fact table.
The mechanism needs to be resilient as:<br>
-	removing a file from the sales folder does not create an error for missing files.<br>
-	adding a new yearly sales file will automatically be loaded in the fact query upon refresh.

# 2. Data Modeling:
<b>Task 2.1:</b><br> 
Do the respective transformations to the Sales fact table in order to split the Country form the City in field “Location”. Make sure you set up the correct Data Type to allow Geo maps.<br><br>
Do the necessary updates in the Date field to make sure you can setup the Date format.<br><br>
<b>Task 2.2:</b> <br>
Create unique key (GeoKey) in Sales and Geography table

<b>Task 2.3:</b> <br>
The Dimensional queries SalesRep and Sub Category need additional treatment. Create a small function that removes the “ID - ” part of these columns that you can invoke and reuse for these two queries to clean the IDs.

<b>Task 2.4:</b> <br> 
Create the Data Model connecting all tables and using the Calendar table already set up in the pbix.

# 3. DAX calculations
<b>Task 3.1:</b> <br>
Calculate Total Revenue in Sales table, using the Product’s Retail Price, and multiplying it by the Units.<br>

<b>Task 3.2:</b> <br>
Calculate Total Cost in Sales table, using the Product’s Standard Cost, and multiplying it by the Units.<br>

<b>Task 3.3:</b> <br>
Calculate Gross Profit in Sales: Total Revenue – Total Cost <br>

<b>Task 3.4:</b> <br>
Calculate a Gross profit MoM growth Change% measure that could benefit us in decision making <br>

<b>Task 3.5:</b> <br>
Calculate a measure for AVG sales per day – this is the average sum of Total Revenue per day based on the Dates of actual Sales.	 <br>

<b>Task 3.6: </b> <br>
-	Breakdown Analysis by Product (drop or increase) <br>
-	This is QBR Report. So QoQ Growth is required

# 4. Use the measures and calculations to assemble a sales reports with different visuals to best show the Sales Insights in one page Dashboard.

Feel free to use your imagination to best represent the data you have available. If you plot Month on x-axis, make sure the months are sorted from Jan-Dec.
