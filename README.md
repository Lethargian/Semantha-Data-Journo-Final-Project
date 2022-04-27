# Oakland Potholes: slowly fixing the problem
Semantha Norris (5/4/22)

!['Oakland Pothole Service Requests by Year', 'Graph of Oakland pothole service requests by year'](/Oakland_ServiceReq_Year.jpg)

# Data Analysis 
1. What year had the most services requests?
    * A: 7 of the 10 months with the highest service requests were in 2019. The entire year of 2019 had 5,767 service requests. 
2. Has the number of service requests increased or decreased?
    * A: Number of requested peaked in 2019, and since 2019 the number of service requests has gone down. 
    * This could be in part due to less people driving during the pandemic.
    * It could also be because of the paving work being done by the City. 
3. Where are the locations with the most service requests?
4. What percentage of service requests have been addressed? What percentage of service requests remain open?
   * A: 
6. Q5

## Q1 - What year had the most services requests?

1. split the DATETIMEINT into two separate columns
  * duplicate the column
  * select the duplicated column
  * GO TO: Data > Split text > detect automatically
  * Rename new columns DATE and TIME respectively

!['Q1-img-01', 'Screenshot of splitting DATETIMEINT into two separate columns'](/Q1-img-01.jpg)

2. Repeat step 1 on the new DATE column
   * duplicate the column
   * select the duplicated column
   * GO TO: Data > Split text > custom detector " / "
   * Rename new third column YEAR and delete the other two

!['Q1-img-04', 'Screenshot of splitting data into year'](/Q1-img-04.jpg)

3. Create a Pivot table to view by month:
  * ROW = DATE, sort by VALUES Z-A
  * Values = REQUESTID, summurized by COUNTA

!['Q1-img-02', 'Screenshot of pivot table settings for Q1'](/Q1-img-02.jpg)

!['Q1-img-03', 'Screenshot of the sorted pivot table for Q1'](/Q1-img-03.jpg)

4. Create a Pivot table to view by year:
  * ROW = YEAR, sort by VALUES Z-A
  * Values = REQUESTID, summurized by COUNTA

!['Q1-img-05', 'Screenshot of pivot table settings for Q1 by year'](/Q1-img-05.jpg)

!['Q1-img-06', 'Screenshot of the sorted pivot table for Q1 by year'](/Q1-img-06.jpg)

## Q2 - Has the number of service requests increased or decreased?

1. Compare the data from Q1 

## Q3 - Where are the locations with the most service requests?

## Q4 - What percentage of service requests have been addressed? What percentage of service requests remain open?

## Q5 - 





