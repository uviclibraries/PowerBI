---
layout: default
title: 2 DAX
nav_order: 1
parent: Workshop Activities
---
# Part 2 DAX

If you expand all the tables in your data pane (located on the right-hand side of the window), your data should look like this. Notice that you now have duplicated columns. We need those for connections, but not to build our measures and visualizations with.
<p float="left">
<img src="images\datapane.png" width="45%">
<img src="images\datapanewithcircles.png" width="45%">
</p>

Step 1: We are going to hide the duplicated columns from the vgsales table, so we don't accidentally use the wrong ones.

> NOTE: you should do the following steps in the "Report view" for the drop-down options you need
<img src="images\reportmode.png" style="">

1. right click on genre and select hide from the drop-down menu. do the same for all the columns that were added to dimension tables
2. right click anywhere in the "Data" Pane and make sure "view hidden" is unselected

    <details><summary><b>Click here for help with step 2</b></summary>
    <img src="images\hidegenreinvgsales.png" style="">
    <img src="images\allhidden.png" style="">
    <img src="images\hidehiddenvars.png" style="">

    </details>

Step 2: Create a measures table. It's best practice to keep a table with only measures in it. 

<blockquote>
A "measure" in Power BI is a custom calculation that performs calculations on your data, dynamically aggregating values from one or more columns
</blockquote><br>

1. on the home tab, choose "Enter Data" from the top pane
2. don't change anything in the table, but rename it "KeyMeasures"
3. click the "Load" button
4. in the "Data" pane select the table by clicking the table name
5. under the "Table tools" tab, select "new measure" a dialogue box will appear. In the box you can write a measure.
6. make a measure for the sum of European sales:
     
        European Sales = SUM(vgsales[EU_Sales])
    click the green checkmark or enter when you are done.

    <details><summary><b>Click here for help with parts 1-6</b></summary>
    <img src="images\enterdata.png" style="">
    <img src="images\createkeymeasurestables.png" style="">
    <img src="images\selectkeymeasuresbyclickingonit.png" style="">
    <img src="images\newmeasure.png" style="">
    <img src="images\dax breakdown.png" style="">

    </details><br>

7. in the *KeyMeasure* column, delete column1 by right clicking on the column name and selecting "Delete from model". 
    <details><summary><b>help</b></summary>
    <img src="images\deletcolfromkeymeasures.png" style="">
    </details>
    Notice how the table name moves to the top of the "Data" Pane and the icon changed. PowerBI now officially recognizes it as a measure table.

    <img src="images\tablebecomesmeasurestable.png" style="">


8. Make a measure for each of the following, each time selecting New Measure
    - SUM of global sales
    - SUM of Japanese sales
    - SUM of North American Sales
    - DISTINCTCOUNT of name (the number of unique games)
    - SUM of other sales
    - AVERAGE rank

    <details><summary><b>Click here for help with DAX codes for part 7</b></summary>
    <code>
    Global Sales = SUM(vgsales[Global_sales])
    </code><br>

    <code>
    Japanese Sales = SUM(vgsales[JP_Sales])
    </code><br>

    <code>
    North American Sales = SUM(vgsales[NA_Sales])
    </code><br>

    <code>
    Count of Games = DISTINCTCOUNT(vgsales[Name])
    </code><br>

    <code>
    Other Sales = SUM(vgsales[Other_Sales])
    </code><br>
 
    <code>
    Average Rank = AVERAGE(vgsales[Rank])
    </code>

    </details>

By the end of these steps you should have a measures table that looks like this:

<img src="images\allmeasures.png" style="">

[NEXT STEP: Visualizations ](3-Visualizations.md){: .btn .btn-blue }
