# Create Data Views

## Objectives <a href="#objectives" id="objectives"></a>

* Understand the Data View UI
* Understand the basic settings of visit definition
* Understand Attribution and Persistence within a Data View

## Data View

With your connection done, you can now progress to influencing visualization. A difference between Adobe Analytics and CJA, is that CJA needs a Data View in order to clean and prepare the data before visualization.

A Data View is similar to the concept of Virtual Report Suites in Adobe Analytics, where you define context-aware visit definitions, filtering and also, how the components are called.

You’ll need a minimum of one Data View per Connection. However, for some use-cases, it’s great to have multiple Data Views for the same connection, with the goal of giving different insights to different teams.\
If you want your company to become data-driven, you should adapt how data is viewed in each team. Some examples:

* UX metrics only for the UX Design team
* Use the same names for KPIs and Metrics for Google Analytics as for Customer Journey Analytics so that the digital analytics team can speak 1 language only.
* Data View filtered to show for instance data for one market only, or one brand, or only for Mobile Devices.

On the **Connections** screen, check the checkbox in front of the connection you just created. Click on the icon to **Create Data View** in the blue bar across the bottom of the screen.

You'll be redirected to the **Create Data View** workflow

## Data View Definition&#x20;

You can now configure the basic definitions for your Data View.

The **Connection** you created in the previous exercise is already selected.&#x20;

If you did not create a new Connection, you can use the Connection previously created: `[Your name] -Data Connection HOL`

1. Give your Data View a name following this naming convention: `[Your name] - HOL Data View`
2. For the time, select the timezone **Greenwich Mean Time; Monrovia, Casablanca \[GMT]**. This is a really interesting setting as some companies operate in different countries and geographies. Allocating the right time zone for each country will avoid typical data mistakes such as believing that for instance, in Peru, the majority of the people buy T-shirts at 4:00 AM.
3. You can also modify the main metrics naming (Person, Session and Event). This is not required but some customers like to use People, Visits and Hits instead of Person, Session and Events (default naming convention from Customer Journey Analytics)

You should now have the following settings configured:

<figure><img src="../.gitbook/assets/Screenshot 2023-04-24 at 15.12.29 (1).png" alt=""><figcaption></figcaption></figure>

Select **Save and Continue.**

## Data View Components

In this exercise, you'll configure the components you need to analyse the data and visualise it using Analysis Workspace. In this UI, there are three main areas:&#x20;

* Left side: Available components from the selected datasets
* Middle: Added components to the Data View
* Right Side: Component settings

You now have to drag and drop the components you need for the analysis to the **Components Added**. To do this, you need to select the components in the left menu and drag and drop them onto the canvas in the middle.

* Let’s start with the first component: **Page** **Name (web.webPageDetails.name)**. Search for this component, then drag and drop it onto the canvas.
* This component is the page name, as you can derive from reading the schema field `(web.webPageDetails.name)`.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-24 at 15.17.17.png" alt=""><figcaption><p>Data View Components - Adding the Page Name Variable</p></figcaption></figure>

Something really important is the **Persistence settings**. The concept of eVars and prop doesn’t exist in CJA but the Persistence settings make a similar behaviour possible.

If you don’t change these settings, CJA will interpret the dimension as a **Prop** (hit level). Also, we can change the Persistence to make the dimension an **eVar** (persist the value across the journey).

Let’s leave the Page Name as a Prop. As such, you don’t need to change any **Persistence Settings**.

**Note:** Persistence settings on metrics can also be changed in Analysis Workspace. In some cases you may choose to set it here to avoid business users from having to think which is the best persistence model.

Next, you’ll have to configure all of your Dimensions and Metrics that you want in your Dataview. Since we have limited time in our Hands on Lab we will add all Dimensions and Metrics to out DataView.

1. Ensure **Contains data** is applied as a filter under the Search bar
2. Select **Add all** next to Schema Fields.

Your configuration should then look like this (Note, you may want to make the names of some variables more user friendly):

<figure><img src="../.gitbook/assets/Screenshot 2023-04-24 at 15.17.17 (1).png" alt=""><figcaption></figcaption></figure>

* Don't forget to **Save** your Data View. Click **Save and Continue** now.

## Data View Settings

You should be redirected to the Data view settings screen.

In this tab, you can modify some important settings to change how data is processed. Let’s start by setting the **Session Timeout** to 30 min. Thanks to every experience event’s timestamp you can extend the concept of a session across all channels. For instance, what happens if a customer calls the call-center after visiting the website? Using custom Session Timeouts you have loots of flexibility in deciding what a session is, and how that session will merge data together.&#x20;

In this tab you can modify other things like filtering the data by using a segment/filter. You won’t need to do that in this exercise.

* In this case, we will keep the default settings.
* Once you are done, please click **Save and finish**.

{% hint style="info" %}
You can come back to this Data View afterwards and change settings and components at any time. Changes **will** affect how historical data is shown.
{% endhint %}

## Objectives <a href="#objectives" id="objectives"></a>

* Understand the Data View UI
* Understand the basic settings of visit definition
* Understand Attribution and Persistence within a Data View

A Data View is similar to the concept of Virtual Report Suites in Adobe Analytics, where you define context-aware visit definitions, filtering and also, how the components are called.

You’ll need a minimum of one Data View per Connection. However, for some use-cases, it’s great to have multiple Data Views for the same connection, with the goal of giving different insights to different teams.\
If you want your company to become data-driven, you should adapt how data is viewed in each team. Some examples:

* UX metrics only for the UX Design team
* Use the same names for KPIs and Metrics for Google Analytics as for Customer Journey Analytics so that the digital analytics team can speak 1 language only.
* Data View filtered to show for instance data for one market only, or one brand, or only for Mobile Devices.

On the **Connections** screen, check the checkbox in front of the connection you just created. Click on the icon to **Create Data View** in the blue bar across the bottom of the screen.

You'll be redirected to the **Create Data View** workflow

## Data View Definition&#x20;

You can now configure the basic definitions for your Data View.

The **Connection** you created in the previous exercise is already selected.&#x20;

If you did not create a new Connection, you can use the Connection previously created: `[Your name] -Data Connection HOL`

1. Give your Data View a name following this naming convention: `[Your name] - HOL Data View`
2. For the time, select the timezone **Greenwich Mean Time; Monrovia, Casablanca \[GMT]**. This is a really interesting setting as some companies operate in different countries and geographies. Allocating the right time zone for each country will avoid typical data mistakes such as believing that for instance, in Peru, the majority of the people buy T-shirts at 4:00 AM.
3. You can also modify the main metrics naming (Person, Session and Event). This is not required but some customers like to use People, Visits and Hits instead of Person, Session and Events (default naming convention from Customer Journey Analytics)

You should now have the following settings configured:

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption><p>Data View Configuration</p></figcaption></figure>

Select **Save and Continue.**

## Data View Components

In this exercise, you'll configure the components you need to analyse the data and visualise it using Analysis Workspace. In this UI, there are three main areas:&#x20;

* Left side: Available components from the selected datasets
* Middle: Added components to the Data View
* Right Side: Component settings

You now have to drag and drop the components you need for the analysis to the **Components Added**. To do this, you need to select the components in the left menu and drag and drop them onto the canvas in the middle.

* Let’s start with the first component:**Name (web.webPageDetails.name)**. Search for this component, then drag and drop it onto the canvas.
* This component is the page name, as you can derive from reading the schema field `(web.webPageDetails.name)`.
* However, using **Name** as the name is not the best naming convention for a business user to quickly understand this dimension.
* Let’s change the name to be **Page Name**. Click on the component and rename it in the **Component Settings** area.
