### Tax analysis using Claude

In this introduction we will be using income tax data.https://drive.google.com/drive/folders/1qksHcinbcy1tU_E4Ak13hQca8sXnjtfq?usp=sharing

First, just follow along with the slides.  When the slides are finished you can attempt the following questions independently.



1. Start by creating a new sheet named "State Data" that saves the percentage of all tax returns that are from elderly tax payers. The new sheet should have the states listed alphabetically and should only include the 50 states.  You want the percentage column to be filled with a formula not the result.

2. Next, in the same sheet create a 'Middle Class' column for the percentage of earners making between $50-100 thousand as well as a 'High Income' column that will be the percentage of taxpayers earning more than $1 million a year.  These results should be formulas and not static numbers.

3. Now, go through and create a new sheet with the same columns except do them without the assistance of Claude.   Were the answers the same?  If not, can you see why errors occurred.
   When using following formula to recreate a new sheet with excel:
    Total Returns: =INDEX(Raw_Data!B$10:VL$10, MATCH(UPPER(A2), Raw_Data!B$3:VL$3, 0))
    Elderly Returns: =INDEX(Raw_Data!C$24:VM$24, MATCH(UPPER($A2), Raw_Data!C$3:VM$3, 0))
    Elderly% of Total: =ROUND(C2/B2*100, 2)
    % of Middle Class: =ROUND((INDEX(Raw_Data!B$10:VL$10, MATCH(UPPER($A2), Raw_Data!B$3:VL$3, 0)+5) + INDEX(Raw_Data!B$10:VL$10, MATCH(UPPER($A2), Raw_Data!B$3:VL$3, 0)+6)) / B2 * 100, 2)
    % of High Income: =ROUND(INDEX(Raw_Data!B$10:VL$10, MATCH(UPPER($A2), Raw_Data!B$3:VL$3, 0)+10)/B2*100, 2)
   When column A is named State, the result is the same.
   
   

5.  Once Claude's sheet is correct, prompt Claude to use that data to create a dashboard.

## Tax Filling Demographics: Tax Year 2016
<img width="1057" height="670" alt="image" src="https://github.com/user-attachments/assets/88ba508d-1683-4cf1-b699-4d1f5e2a3024" />

## Key Takeaways

1. Four states exceed 27% elderly filling share
2. States in the North east such as connecticut, New York, Massachusetts and New Jersey have highest millionaire filer rate.
3. States in the South  for instance, Missisippi, Florida, New mexico, Louisiana and Geogia appear in the bottom 5 for middle-class filer rate suggesting polarized income distribution, in which more people are clustered at teh low end or the high end with fewer in the middle class population.
