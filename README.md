# Analysis on Sachin Tendulkar's ODI Record

### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Change the type of Runs, Wickets, Runs Conceded, Catches from text to whole number, so that we can perform calculations on them.

- Step 4 : A new column 100/50 was created with the following condition

      if runs are more than or equal to 200 then double century,
      if runs are more than or equal to 100 then century,
      if runs are more than or equal to 50 then half century,
      else ' '
 
- Step 5 : A new column out was created with the following condition

      if batting_score contains '*' or DNB or TDNB then Not Out,
      else Out

- Step 6 : In the report view, text box was added where title "Sachin Tendulkar's ODI Record" was mentioned.
- Step 7 : Cards were added from the visualizations pane in report view to represent total matches, total runs, average, total wickets, total catches, highest score. 

- Step 8 : Visual filters (Slicers) were added for three fields named "Year", "Opposition" & "Ground".
- Step 9 : Three donut charts were added to the canvas, representing Centuries,Runs by innings, results.
- Step 10 : A line chart was also added to the report design area representing the runs scored per year.
- Step 11 : Table was used to represent Top 10 performances.
- Step 12 : A bar chart was added to represent runs scored against different countries.

### Calculations and DAX used

- Created a measure 'average' using below formula

      Average = 
      DIVIDE(
        SUM(sachin_odi[Runs]),
        COUNTROWS(FILTER(sachin_odi, sachin_odi[Out] = "Out"))
        )

### Analysis

- Sachin played 463 matches in which he scored 18,426 Runs with the average of 44.83 and took 154 wickets where India won 51% of the matches he played, lost 43% and 6% were draw or no result.
- He scored 96 half centuries, 48 centuries and a double century in his ODI career.
- 61% of the match in which he score half centuries were won by India.
- 67% of the match in which he score centuries were won by India.
- Most runs were against Srilanka, Australia and Pakistan.
- Best inninig was against South Africa in 2010 where he scored 200 runs and became the first cricketer to score double century.

 # Report Snapshot

![Dashboard](https://github.com/vinodsrawat/Analysis-on-Sachin-Tendulkars-ODI-Record-PowerBI-Report/assets/161686865/f0161322-b9ec-4aab-9237-36b17911dc8c)
