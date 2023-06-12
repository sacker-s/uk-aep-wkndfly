---
description: >-
  In this exercise, you’ll create a workspace project looking at different data
  points, visualisations and segments.
---

# Prepare Workspaces and Reports

## Objectives

* Understand the Analysis Workspace UI in CJA
* Understand the concepts of data preparation in Analysis Workspace
* Learn how to do data calculations

## Analysis Workspace UI in CJA

Analysis Workspace removes all of the typical limitations of a single Analytics report. It provides a robust, flexible canvas for building custom analysis projects. Drag-and-drop any number of data tables, visualisations, and components (dimensions, Metrics, segments, and time granularities) to a project. Instantly create breakdowns and segments, create cohorts for analysis, create alerts, compare segments, do flow and fallout analysis, and curate and schedule reports for sharing with anyone in your business.

Customer Journey Analytics brings this solution on top of Platform data.&#x20;

## Setting up your Project&#x20;

To get an overview of the available projects to you, click on Workspace. Either click on **'Create new'** for a new workspace project, or select a pre-built project - in this case **'WKND - Lab 3 - Customer'.**

<figure><img src="../.gitbook/assets/Screenshot 2023-04-26 at 07.37.02.png" alt=""><figcaption></figcaption></figure>

## Creating your first panel - Key KPIs

1. First of all, we want to **rename** the project so it's in your name. Click on 'WKND - Lab 3 - Customer' and replace Customer with your name/company. &#x20;
2. There will be a panel set up for you already named **'Key KPIs'.**
3. At any point, you can save your project by going to **Project > Save.**
4. Click on the drop down of **Data Views** on the right hand side of the panel, and select **'WKND - Analysis Dataview'**.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-26 at 08.39.18.png" alt=""><figcaption></figcaption></figure>

5. Finally, select the date range **1st October 2022 - 30th April 2022** from the date selector below the Data View box, and select 'Apply to all Panels'.
6. Now you are ready to start building with Data. Click on **Components** on the left hand side panel, this is the 3rd icon down as shown above.
7. Search for interaction channel, and drag this dimension (orange component) onto the main part of the freeform table, this will automatically upload the data with **'Events'** as the metric.
8. Search for **'People'** in the components list, then drag this in front of Events; search for 'Sessions' in the components list, then drag this in front of People. You can play around with the order of the metrics.
9. Now click on web in the freeform table (this will select that line of data), hold down shift, and select the remaining lines of data in the table so it is all selected. Right click on the table, click on **Visualize, then Donut**. This will build out 3 donuts for you. You can move the donut underneath the data by simply dragging and dropping them.&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2023-04-18 at 15.43.33.png" alt=""><figcaption></figcaption></figure>

9.  You can create more freeform tables with the following data points, and play around with the Visualisations:

    1. Dimensions = Interaction Channel; Metrics = Flight bookings, Flight Cancellations. Flight reschedules (suggestion - select all the data, right click, click on visualization and select horizontal bar).
    2. Dimensions = Interaction Channel; Metrics = Flight check-ins, Kiosk check-ins.
    3. Dimensions = Food Preference; Metrics = Events.
    4. Dimensions = Travel class; Metrics = Events. Now search for Seat preference in Components, drag and drop this under 'economy' to get a further breakdown.



    <figure><img src="../.gitbook/assets/Screenshot 2023-04-18 at 15.58.47.png" alt=""><figcaption><p>You have now completed your first panel.</p></figcaption></figure>

##

