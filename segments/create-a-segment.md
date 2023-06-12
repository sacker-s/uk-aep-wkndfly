---
description: >-
  In this exercise, you’ll create a segment by making use of Adobe Experience
  Platform’s Segment Builder.
---

# Create a Segment

## Segment Overview

{% hint style="info" %}
To log into the Adobe Experience Platform,[ go here](https://experience.adobe.com/#/@adobeamericaspot4/sname:uk-aep-bootcamp/platform/home).
{% endhint %}

To get an overview of available segments in Adobe Experience Platform:

1. In the menu on the left side, click on **Segments**. You will see a dashboard overview with information on a specific segment.
2. Click on **Browse** at the tab bar. You will see an overview of all existing segments.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 17.35.13.png" alt=""><figcaption></figcaption></figure>

## Create A Frequent Flyer Segment

We want to create a segment rule that will select all customer profiles that have booked more than 8 flights in the last year. WKND Fly consider these customers to be frequent flyers and want to personalise content to them.&#x20;

1. Click on **+ Create segment**. This will open the Segment Builder. You will immediately notice the **Attributes** tab selected underneath **Fields**. As well as the **XDM Individual Profile** selector under **BROWSE ATTRIBUTES.**

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 17.39.45.png" alt=""><figcaption></figcaption></figure>

Since XDM is the language that powers the experience business, XDM is also the foundation for the segment builder. All data that is ingested in AEP should be mapped against XDM, and as such, all data becomes part of the same data model regardless of where that data comes from. This gives you a big advantage when building segments, as from this one segment builder UI, you can combine data from any origin in the same workflow.&#x20;

Segments built within Segment Builder can be sent to solutions like Adobe Target, Adobe Campaign and Adobe Audience Manager for activation.

Let's build a segment for our Frequent Flyers:

1. Select the **Events** tab in the Fields section.
2. In the text search field, type **flight booking.** You will see a flight booking listed under **Event Types.**
3. Drag the **flight booking** event type onto the canvas where it says **Start building segments.**
4. Click on the **Booking** event box to open the Event Rule.

Your screen should look like:

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 17.44.49.png" alt=""><figcaption></figcaption></figure>

&#x20;At each step in defining your segment, you can get an estimate of the segment's population:

* Click on **Refresh Estimates**.&#x20;

You will then see an estimation of your current segment size. This is very helpful for a business user, so that they can see the impact of certain attributes on the resulting segment size.

So far, you’ve only used the UI to build your segment, but there’s also a code-option to build a segment.

When building a segment, you’re actually composing a Profile Query Language (PQL) query. To visualise the PQL code,&#x20;

1. Click on the **Code View** switcher in the upper right corner of the segment builder.
2. Click on **Segment Builder view** to return back to the UI.

{% hint style="info" %}
So far your segment will select all customer profiles who have made at least one flight booking at any time. Now we will restrict this further to target only the frequent flyers.
{% endhint %}

1. In the **Event Rule**, change the **include** condition to include `at least`
2. Type `8` into the text field.
3. We also want to specify the time period in which the 8 flight bookings must occur in order to be considered a frequent flyer. In the **Events** panel, change the **Anytime** drop down to `In last 1 Year(s)`

Your final segment condition should look like:&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 17.55.04.png" alt=""><figcaption><p>Frequent Flyer segment condition</p></figcaption></figure>

Finally, let's save our segment.

1. Enter a **Name** for your segment using the following naming convention\
   _`[your name] - Frequent Flyers`_, \
   e.g. `sacker - Frequent Flyers`.
2. (optional) Enter a **Description**.
3. Select **Batch** from the **Evaluation method** dropdown list.
4. Click on **Save and Close**.

You will be taken to the **Segment summary** screen, outlining your segment definition.



{% hint style="success" %}
You have now successfully created a segment using the Adobe Experience Platform Segment Builder.
{% endhint %}

