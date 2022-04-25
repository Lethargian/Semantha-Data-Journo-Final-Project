# Oakland Potholes: slowly fixing the problem
Semantha Norris (5/4/22)


# Data Analysis 
1. What year had the most services requests?
    * A: 7 of the 10 months with the highest service requests were in 2019. The entire year of 2019 had 5,767 service requests. 
3. Has the number of service requests increased or decreased?
    * A: Number of requested peaked in 2019, and since 2019 the number of service requests has gone down. 
    * This could be in part due to less people driving during the pandemic.
    * It could also be because of the paving work being done by the City. 
5. Where are the locations with the most service requests?
6. What percentage of service requests have been addressed? 
7. What percentage of service requests remain open?

## Q1 - What year had the most services requests?

1. split the DATETIMEINT into two separate columns
  * duplicate the column
  * select the duplicated column
  * GO TO: Data > Split text > detect automatically
  * Rename new columns DATE and TIME respectively

!['Q1-img-01', 'Screenshot of splitting DATETIMEINT into two separate columns'](/Q1-img-01.jpg)

2. Create a Pivot table
  * ROW = DATE, sort by VALUES Z-A
  * Values = REQUESTID, summurized by COUNTA

!['Q1-img-02', 'Screenshot of pivot table settings for Q1'](/Q1-img-02.jpg)

!['Q1-img-03', 'Screenshot of the sorted pivot table for Q1'](/Q1-img-03.jpg)

3. Sort by year, highlight the cells in the VALUES column for a particular year and see the SUM at the bottom right corner. 

## Q2 - Has the number of service requests increased or decreased?

1. Use the same method from Q1 step 3 to calculate the totals for each year and enter then into a new spreadsheet

!['Q2-img-01', 'Calculated total service requests per year'](/Q2-img-01.jpg)

## Q3
## Q4
## Q5





