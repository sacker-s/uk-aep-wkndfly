# Journey Analysis Visualisations & Filters

### Objectives <a href="#objectives" id="objectives"></a>

* Understand Analysis Workspace UI
* Learn some feature that make Analysis Workspace so different.
* Learn how to analyse in Customer Journey Analytics using Analysis Workspace

## Context <a href="#context" id="context"></a>

In this exercises you will use Analysis Workspace within Customer Journey Analytics to analyse product views, product funnels, churn etc.

Let’s use the project you just created. Open your project.

With your project opened and the Data View selected, you're ready to start building your first visualisations.&#x20;

## Flow by Channel Report <a href="#context" id="context"></a>

1. Open up the **Multi-Channel Reporting: Journey Analysis** by clicking on the arrow on the left hand side - you will see one visualisation there already.
2. Select **Flow** from the visualisations list on the left hand side - drag and drop this into the panel above the existing visualisation.
3. In the 'contains' box in the middle, select interaction channel, then click **build**. This will now build out your visualisation automatically.&#x20;
4. Click on 'Callcenter' on the right hand side to expand the flow one more time and the report should look like this

<figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 15.30.57 (1).png" alt=""><figcaption></figcaption></figure>

6. If you want to break down the call centre channel by call reason, right click on the one you just expanded, then click breakdown, then dimensions and search for **Call Reason**. This will bring up a box below with the call reasons why customers on this particular path, called in.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 15.32.35.png" alt=""><figcaption></figcaption></figure>

7. You can play around with adding filters in at this stage, or breaking down other routes.

## Building a Filter <a href="#context" id="context"></a>

Filters are the same as Segments in Adobe Analytics, just renamed. And once these filters are built in CJA, they are automatically shared on platform, so you can use them in CDP for example.

1. On the left hand column, click on the **+ next to filters** to create a new filter.
2. Drag and drop the metric **'booking confirmations'** and ensure the logic reads **'equals 1'.**
3. Drag and drop the metric **'Flight check-ins'** and change the logic to **'is less than 1'.**
4. On the right hand side, you will see a preview of the number of people who fit this category. Once you are happy with the segment, name it and save it down.
5. Apply this to the **Flight Fallout** report and see how the data changes.

