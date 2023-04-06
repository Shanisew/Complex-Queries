# Complex-Queries

1.   Using In-Line Views
a.   Produce a report of Orion Star sales force employees’ aggregate sales in 2007. Select Country, First_Name, Last_Name, Value_Sold, Orders, and Avg_Order columns by joining orion.Order_Fact and orion.Sales tables on Employee_ID. Group the report by Country, First_Name, Last_Name. Include only employees having an aggregate Value_Sold of $200.00 or more. Order the results by Country, Value_Sold (descending), and Orders (descending).
1)   Calculate Value_Sold by summing Total_Retail_Price.
2)   Calculate Orders by using the COUNT(*) function to count the number of rows returned for each employee.
3)   Calculate Avg_Order by dividing Value_Sold by Orders.
4)   Title the report (use two lines), the first line should read  2007 Sales Force Sales Statistics and the second line should read For Employees With 200.00 or More In Sales
Requested Output:
 
b.   Using the query created in step a as an in-line view, select Country, the maximum Value_Sold, Orders, and Avg_Order as well as the minimum Avg_Order for each country. Name the report 2007 Sales Summary by Country.
Hint: An in-line view must not use the ORDER BY clause.
Requested Output:
 
2.   Building Complex Queries with In-Line Views
Your ultimate goal in this exercise is to create a report showing each employee’s salary expressed as a percentage of the total salary for his department. The report should be sorted by department and, within each department, in descending order of salary percentage.
•	The orion.Employee_Payroll table contains Salary.
•	The orion.Employee_Addresses table contains Employee_Name.
•	The orion.Employee_Organization table contains Department.





Sketch of desired report:
Employee Salaries as a percent of Department Total

Department               Employee_Name                     Salary  Percent
Accounts                   Mea, Azavi0us                   58,200.00     8.6%
Accounts                   Miller, Pamela                    53,475.00     7.9%
Accounts                   Asta, Wendy                      52,295.00     7.7%
a.   Create a report aggregating the sum of all salaries for each department. The report should include Department and the sum of all associated salary values as Dept_Salary_Total. Join orion.Employee_Payroll and orion.Employee_Organization by Employee_ID to obtain the information you need.
•	The orion.Employee_Payroll table contains salary values.
•	The orion.Employee_Organization table contains department information.
Requested output (partial):
 
b.   Create a report that includes the employee ID, name, and department. Join orion.Employee_Addresses and orion.Employee_Organization by Employee_ID to obtain the information you need.
•	The orion.Employee_Addresses table contains Employee_Name and Employee_ID.
•	The orion.Employee_Organization table contains Employee_ID and Department.

Requested output (partial)
 
c.   Use the two queries you created in steps a and b as in-line views. Join the views with orion.Employee_Payroll by either Employee_ID or Department to create the final report.
•	The query from step a contains Department and Dept_Salary_Total.
•	The query from step b contains Employee_ID, Employee_Name, and Department.
•	The orion.Employee_Payroll table contains Employee_ID and individual Salary values.
Requested Output (Partial)
 
3.   Building a Complex Query Using a Multi-Way Join
Create a report using a multi-way inner join, which produces the total of the 2007 sales figures for each Orion Star employee. The report should be titled 2007 Total Sales Figures and must include both the managers’ and employees’ names (displayed as first name followed by last name), and the total retail value of all sales made by each employee in 2007. Present the information as follows:
•	Use one row per employee.
•	Organize the report so that the following standards are observed:
	Employees under one manager are adjacent to each other (grouped together) on the report.
	Within each manager’s group, employees are listed in decreasing order of total sales.
	The Australian groups are listed first, followed by the U.S. groups.
	Manager names are in alphabetical order by last name and then first name.
Remember that you can group and order by columns that are not included in the SELECT statement list.
The data that you need can be found in the following tables (variables of interest in parentheses):
•	orion.Order_Fact (Employee_ID, Total_Retail_Price)
•	orion.Employee_Organization (Employee_ID, Manager_ID)
•	orion.Employee_Addresses (Employee_ID, Employee_Name)
Requested Output (Partial):
 
![image](https://user-images.githubusercontent.com/101452475/230446387-ea1f2542-37ff-45cd-9102-4c1d17e8fb45.png)
