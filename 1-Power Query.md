---
layout: default
title: 1 Power Query
nav_order: 1
parent: Workshop Activities
---
# Part 1 Power Query

>Step 0: **_DOWNLOAD_** by [going to vgsales.csv on GitHub](https://github.com/uviclibraries/PowerBI/blob/main/Data/vgsales.csv) click the download button in the top right-hand corner
!

<img src="images\image.png" style="">

## Reminder

In Power Query we want to transform the data to make it compatible with Power BI, so it's closely related to the relationship and model building part of Power BI. We can also do some data cleaning in Power Query, although it is not its main function.

Step 1: loading in the data
- in Power BI select New "blank report"
- under the home Tab select "get data" and choose "Text/CSV"
- find the where you saved "vgsales.csv" and open it
- choose "Transform Data"

<details><summary><b>Click here for pictures to help you through step 1</b></summary>
<img src="images\newreport.png" style="">
<img src="images\getdata.png" style="">
<img src="images\choosefile.png" style="">
<img src="images\transformdatabuton.png" style="">
</details>

<br>

Step 2: transforming the data

<blockquote>

We want to transform the data to work in a star schema. I often think of the "points" of the star as being the categories (qualitative)  that will filter the data and the core of the star being where the data measures (quantitative) will be, along with connections to the points. Looking at the columns in your dataset, which do you think would be filter categories?
<br><br>
Here are descriptions for the columns: <br><br>

Rank - Ranking of overall sales for a game<br>

Name - The game name<br>

Platform - Platform of the game's release<br>

Year - Year of the game's release<br>

Genre - Genre of the game<br>

Publisher - Publisher of the game<br>

NA_Sales - Sales in North America (in millions)<br>

EU_Sales - Sales in Europe (in millions)<br>

JP_Sales - Sales in Japan (in millions)<br>

Other_Sales - Sales in the rest of the world (in millions)<br>

Global_Sales - Total worldwide sales<br>

</blockquote>

To make your dimension tables (the points of your star)
1. right click on the **vgsales** query in the Queries pane
2.  choose reference, this creates a duplicate table that is still connected to the first table
3. choose one of the categories that will be a dimension
4. right click on the column header and choose "remove other columns". ***NOTE that dimension tables often have multiple columns but in this example each dimension table only has one column**
5. right click on the column header again and select "remove duplicates"
6. now rename the table under the "Query Settings" pane to something reflective of your selected column
7. repeat steps 1-6 for all the dimension tables. Eventually you should have the following tables
    - vgsales
    - Platforms
    - Years
    - Genres
    - Publishers

Make your years column a number type. This will help with sorting and filtering
1. in the *vgsales* table, change the data type of **Year** to whole number by clicking on the symbol on the left-hand side of the column header
2. replace the errors with nulls by right clicking on the Year header and selecting "replace errors" replace them with "null"
3. in the *Year* table filter out the null by clicking on the arrow on the right-hand side of the column header and un-selecting (null)

<details><summary><b>Click here for pictures to help you through step 2</b></summary>
<img src="images\lookatcolumns.png" style="">
<img src="images\reference.png" style="">
<img src="images\removeothercols.png" style="">
<img src="images\removeduplicates.png" style="">
<img src="images\renamequery.png" style="">
<p>in the vgsales table</p>
<img src="images\changetypes.png" style="">
<img src="images\replaceerrors.png" style="">
<img src="images\replaceeerrorspopup.png" style="">
<p>in the Years table</p>
<img src="images\filternulls.png" style="">
</details>

<br>

Step 3: load in the data and check the model
- on the home tab, click "Close & Apply"
<img src="images\closeandapply.png" style="">
- check out the "star" schema that should have auto created under the model tab in the Power BI editor

<img src="images\modelview.png" style="">

Looking at the model

>notice the connecting lines in the schema show a 1-to-many relationship (1 at one end and * at the other end) and have an arrow in the centre of the line, that shows the direction of the relationship. We have all 1-to-many relationships, which is what we want.


[NEXT STEP: Dax ](2-DAX.md){: .btn .btn-blue }
