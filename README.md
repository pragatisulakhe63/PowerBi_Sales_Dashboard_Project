1) Assemble a sales reports with different visuals to best show the Sales Insights in one page Dashboard.
          1.	Sales (folder by year)
          2.	Categories (Excel)
          3.	Geography (Excel)
          4.	Product (CSV / Database)
          5.	SalesRep (Excel)
          6.	SubCategories (Excel)
Task 1.1:
Create a mechanism to load all the files from the sales folder in a single Sales fact table.
The mechanism needs to be resilient as:
	-removing a file from the sales folder does not create an error for missing files.
	-adding a new yearly sales file will automatically be loaded in the fact query upon refresh.
 
2.	Data Modeling:
Task 2.1: 
Do the respective transformations to the Sales fact table in order to split the Country form the City in field “Location”. Make sure you set up the correct Data Type to allow Geo maps.
Do the necessary updates in the Date field to make sure you can setup the Date format.
Task 2.2: 
Create unique key (GeoKey) in Sales and Geography table

Task 2.3:
The Dimensional queries SalesRep and Sub Category need additional treatment.

 
Create a small function that removes the “ID - ” part of these columns that you can invoke and reuse for these two queries to clean the IDs.
Task 2.4: 
Create the Data Model connecting all tables and using the Calendar table already set up in the pbix.

3.	DAX calculations
Task 3.1:
Calculate Total Revenue in Sales table, using the Product’s Retail Price, and multiplying it by the Units.
Task 3.2:
 Calculate Total Cost in Sales table, using the Product’s Standard Cost, and multiplying it by the Units.
Task 3.3:
Calculate Gross Profit in Sales: Total Revenue – Total Cost
Task 3.4:
Calculate a Gross profit MoM growth Change% measure that could benefit us in decision making
Task 3.5:
Calculate a measure for AVG sales per day – this is the average sum of Total Revenue per day based on the Dates of actual Sales.	
Task 3.7: 
-	Breakdown Analysis by Product (drop or increase)
Calculate the following time measures:
-	This is QBR Report. So QoQ Growth is required
4.	Use the measures and calculations to assemble a sales reports with different visuals to best show the Sales Insights in one page Dashboard.
