---
description: >-
  In this exercise we'll be creating a segment that we'll be using in our
  journey
---

# Creating a segment

{% hint style="info" %}
If you don't want to create the segment, you can use a segment that has already been created: **Onboarding - Flight Departure in next 24 hours**
{% endhint %}

## Segment overview

To get an overview of all segments in Adobe Journey Optimizer:

1. In the menu on the left side, click on **Segments**. You will see an overview with all existing segments.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 12.06.34.png" alt=""><figcaption></figcaption></figure>

## Creating a segment

We'll be creating a segment that contains all customers that are booked onto a flight that departs in the next 24 hours.

Click on **Create segment**. You'll be taken to the **Segment builder**.

1. Set the **name** to `[your name] - Flight departure in next 24 hours`.
2. Set the **evaluation method** to `Edge`.
3. In the **Events** tab, search for `departure date`.
4. You will see two results, one for flight search and one for flight reservations. Drag the **Departure Date** that is part of the Flight Reservations XDM Object onto the middle section (_XDM Experience Event > Reservations > Flight Reservations > Departure Date_).
5. In the Event Rule Change **Today** to `In next 1 Day(s)`.
6. Your screen should look like the image below. Click **Save and Close** to finish your segment.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 12.13.39.png" alt=""><figcaption><p>Segment Rule for profiles that are flying in the next 24 hours</p></figcaption></figure>

{% hint style="success" %}
You have now successfully created your segment to qualify Profiles for your Journey.
{% endhint %}
