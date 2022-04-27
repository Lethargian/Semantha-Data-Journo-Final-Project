# Oakland Potholes: slowly fixing the problem
Semantha Norris (5/4/22)

!['Oakland Pothole Service Requests by Year', 'Graph of Oakland pothole service requests by year'](/Oakland_ServiceReq_Year.jpg)

# Data Analysis 
1. What year had the most services requests? Has the number of service requests increased or decreased?
    * A: 7 of the 10 months with the highest service requests were in 2019. The entire year of 2019 had 5,767 service requests. 
    * A: Number of requested peaked in 2019, and since 2019 the number of service requests has gone down. 
    * This could be in part due to less people driving during the pandemic.
    * It could also be because of the paving work being done by the City. 
2. What percentage of service requests have been addressed? What percentage of service requests remain open?
   * A: 68% of all request have been closed. 14% remain open. 
3. What have these percentages been over the last 3 years (since the pandemic started)?
   * A: 2020 is similar to the overal ratio, with 13% open and 68% closed
   * 2021 = 30% open and 56% closed
   * 2022 = 60% open and 19% closed
4. Where are the locations with the most service requests?
5. Have the most problematic locations been addressed by the city?

## Q1 - What year had the most services requests? Has the number of service requests increased or decreased?

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
   * Rename column F "YEAR" and delete colums D&E

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

## Q2 - What percentage of service requests have been addressed? What percentage of service requests remain open?

1. Create a Pivot table to view by month:
   * ROWS = STATUS
   * Values = REQUESTID, summurized by COUNTA, shown as "% of grand total"

!['Q2-img-03', 'Screenshot of pivot table for Q2'](/Q2-img-03.jpg)
!['Q2-img-02', 'Screenshot of pivot table settings for Q2'](/Q2-img-02.jpg)

## Q3 - What has the open to closed ratio been over the last 3 years (since the pandemic started)?

1. Duplicate the pivot table from Q2
2. Add a COLUMN = YEAR
3. Change VALUES settings to be "% of column"

!['Q3-img-01', 'Screenshot of pivot table settings for Q3'](/Q3-img-01.jpg)
!['Q3-img-02', 'Screenshot of pivot table Q3'](/Q3-img-02.jpg)

## Q4 - Where are the locations with the most service requests?

## Q5 - Have the most problematic locations been addressed by the city?





