---
layout: default
title: 3 Visualizations
nav_order: 1
parent: Workshop Activities
---
# Part 3 Visualizations

In this visualization stage, you have more freedom to play around, as you have now formatted your data to work well within the visualizations.

The visualization pane shows icons representing the different visualizations. If you hover over an icon, the name of the visualization shows in the tooltip.

<img src="images\visualizationspanehoverforname.png" style="">

Step 1: add the data to a visualization
1. click on an icon from the visualizations pane. 
        
    NOTE: I would suggest one of the first 4 bar charts, the line chart or one of the pie charts to start, as they are the easiest to work with. In the example below, I use the clustered column chart.
2. take a look at the field boxes that appear in the visualization pane when you create a visualization. Each of these boxes either expects a measure (ie Global Sales), or a field value (ie Genre).

    <img src="images\visualizationspanefieldsempty.png"><br>

    NOTE: if a measure is expected, but you drag a field in, it might automatically convert the field to a measure (ie Count of Genre). Watch out for that as you are playing around.
    <img src="images\autoaggregate.png">

3. drag measures and fields from the data pane into the data field boxes in the visualizations pane. Play with moving the data around and adding different data to see what happens.

    NOTE: your visualization should have at least one measure from your KeyMeasures table, or the fields wont properly connect with each other. This is because of the way we built our model (and the directions of the relationships)

    <details><summary><b>Click here for a video to help you through step 1</b></summary>
    <video src="images\filling the fields in a visualization.mp4" width="100%" height="100%" controls></video>
    </details>


Step 2: format your visualization

Once your visualization contains the data you'd like it to, you can add more formatting to improve it.

1. with your visualization selected, select the second icon under "Build Visual" in the "Visualizations" pane (it looks like a bar chart with a paint brush)
2. Play around with the formatting in the "Visual" section. You can do things like:
    - change the axes ranges
    - change the axis label font
    - change the bar, line, or slice colours
    - add labels
    - add or remove grid lines

    <details><summary><b>Click here for a video to help you with formatting in the "visual" section</b></summary>
    <video src="images\playingwithvisualizationformatting.mp4" width="100%" height="100%" controls></video>
    </details>

3. there is also a section called "General". This is the same for all visualizations. You can do things like:
    - change and format the title
    - add backgrounds
    - change the tooltip source
    - add alt text

    <details><summary><b>Click here for a video to help you with formatting in the "General" section</b></summary>
    <video src="images\playingwithgeneralvizformatting.mp4" width="100%" height="100%" controls></video>
    </details>

Step 3: adding more visualizations

1. add a slicer type visualization. The slicer expects a dimension (the points of the star). Measures will not work.

    <details><summary><b>Click here for a video to help you create and format a slicer</b></summary>
    <video src="images\formattingslicers.mp4" width="100%" height="100%" controls></video>
    </details><br>

2. add more visualizations to your page. Try exploring different measures and categories in your various visualizations.

3. Add a title and description to your report using the text box

<img src="images\addtextbox.png">

4. Don't forget to save your file!

Congrats, you're done the workshop!


[NEXT STEP: Additional Resources](additional-resources.md){: .btn .btn-blue }
