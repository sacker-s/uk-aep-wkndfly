---
description: >-
  In this exercise, you'll be creating and testing a journey using all the
  component you've created in the previous exercises.
---

# Creating a journey

## Journey overview

To get an overview of all journeys in Adobe Experience Platform:

1. In the menu on the left side, click on **Journeys**. You will see a overview with all existing journeys.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 12.17.06.png" alt=""><figcaption><p>Journey Overview</p></figcaption></figure>

## Creating a journey

We'll be creating a journey that will send a push message to customers when their flight is departing in the next 24 hours. This will be encouraged to check in.

Click on **Create Journey**. You'll be taken to the **Journey canvas** with the journey properties opened.

1. Set the name to `[your name] - Check in journey for loyalty members`.
2. For the other properties we'll keep the default values.
3. Your screen should look like the image below. Click **Ok** to save and close the properties.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 12.20.03.png" alt=""><figcaption><p>Journey Creation - properties</p></figcaption></figure>

You're now in the journey canvas. This is where you'll be creating your journey's logic. In the left menu you have **activities**. There's three types of activities:

**Events** are the triggers that can start or continue your journey.

**Orchestration** is the logic of your journey. It looks at conditions, segments, but can also be used to make your workflow wait or end.

**Actions** are the results of your journey. This can be messages, profiles updates or API calls.

### Segment qualification

1. We're starting our workflow off with a segment entry trigger. From the events tab, choose **Segment qualification** and drag it onto the canvas.
2. Click on the activity to open the detailed view.
   1. Set the **label** to `Flight in next 24 hours`.
   2. Click on the pencil icon next to **Select a segment** to open a window, select your segment from the list and click **Save**. If you didn't create a segment, you can use `Onboarding - Flight Departure in next 24 hours`.
   3. Set the **behaviour**  to `Enter`. This means the journey will start as soon as the customer enters the segment.
   4. Set the **namespace** to `Email(Email)`.
   5. Your screen should look like the image below. Click **Ok**.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 12.23.07.png" alt=""><figcaption><p>Journey Creation - Segment Qualification</p></figcaption></figure>

### Condition - Loyalty Status

1. From the orchestration tab, choose Condition and drag it onto the empty circle on the canvas.
2. Click on the activity to open the detailed view.
   1. Set the **label** to `Loyalty Status`.
   2. Click on **Path1** and change the label to `Bronze and Silver`.
   3. Click on the pencil icon next to **Add an expression** to open a window.
      1. On the left side, unfold **ExperiencePlatform**, find **loyalty** and unfold this,  find `tier` and drag it to the right side.
      2. Set the condition to `equal to` and input `bronze,` click **Ok**.&#x20;
      3. Again, on the left side, drag another `tier` condition to the right side, underneath the condition you just created.&#x20;
      4. Set the second condition to `equal to` and input `silver,` click **Ok**.&#x20;
      5. Click on the `AND` dropdown and change this to `OR`.
      6. Click **Ok** to save the conditions. Your expression should look like:

<figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 12.32.28.png" alt=""><figcaption><p>Check if customer is either bronze or silver Club member</p></figcaption></figure>

1. Click **+Add a path** twice to add two new branches to the Journey
   1. Set the **labels** to `Gold` and `Platinum.`
   2. Open the Expression editor for the Gold path.
   3. On the left side, unfold **ExperiencePlatform**, find **loyalty** and unfold this,  find `tier` and drag it to the right side.
   4. Set the condition to `equal to` and input `gold,` click **Ok**.&#x20;
   5. Open the Expression editor for the Platinum path.
   6. Again, on the left side, drag `tier` condition to the right side.
   7. Set the condition to `equal to` and input `platinum,` click **Ok**.&#x20;
2. Check **Show path for other cases than one(s) above** and set the label to `Not a loyalty member`.
3. Your screen should look like the image below. Click **Ok**.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 12.39.24.png" alt=""><figcaption><p>Journey - Creating a condition</p></figcaption></figure>

### Custom Action message - Time to check in

**Custom actions** enable you to configure connection of a third-party system to send messages or API calls. An action can be configured with any service from any provider that can be called through a REST API with a JSON-formatted payload.

{% hint style="info" %}
In this exercise, we have pre-created a Custom Action that sends messages to a public Webhook. You will reuse this in your Journey.
{% endhint %}

1. From the actions tab, choose **Webhook** and drag it onto the empty circle on the canvas along the `Bronze and Silver` path.
2. Click on the activity to open the detailed view.
   1. Set the **Label** to `Check in message`.
   2. Open the **Action parameters** by clicking the pencil icon. Here we will define the text that will be posted to our Webhook.&#x20;
   3. Click to open **Advanced mode.**
   4. Input the following expression:&#x20;

{% code overflow="wrap" %}
```handlebars
"Time to check in for your flight: " + #{ExperiencePlatform.ProfileFieldGroup.profile._adobeamericaspot4.latestAction.actionProduct} + " - As a WKND Club member you can check in 1 bag for free!"
```
{% endcode %}

{% hint style="info" %}
Note: In the **Action parameters** section, you’ll see the message parameters defined as _“Variable”_. For these parameters, you can define where to get this information (example: events, data sources), pass values manually or use the advanced expression editor for advanced use cases. Advanced uses cases can be data manipulation and other function usage. Refer to this [page](https://experienceleague.adobe.com/docs/journey-optimizer/using/orchestrate-journeys/building-advanced-conditions-journeys/expressionadvanced.html?lang=en).
{% endhint %}

3. Do the same for the `Gold` path
   1. From the actions tab, choose **Webhook** and drag it onto the `Gold` path.
   2. Set the **Label** to `Check in message`.
   3. Open the **Action parameters** by clicking the pencil icon.&#x20;
   4. Click to open **Advanced mode.**
   5. Input the following expression:&#x20;

{% code overflow="wrap" %}
```handlebars
"Time to check in for your flight: " + #{ExperiencePlatform.ProfileFieldGroup.profile._adobeamericaspot4.latestAction.actionProduct} + " - As a Gold member, you can skip the queues and use our priority check in!"
```
{% endcode %}

4. Do the same for the `Platinum` path
   1. From the actions tab, choose **Webhook** and drag it onto the `Platinum` path.
   2. Set the **Label** to `Check in message`.
   3. Open the **Action parameters** by clicking the pencil icon.
   4. Click to open **Advanced mode.**
   5. Input the following expression:&#x20;

{% code overflow="wrap" %}
```handlebars
"Time to check in for your flight: " + #{ExperiencePlatform.ProfileFieldGroup.profile._adobeamericaspot4.latestAction.actionProduct} + ". When you arrive, the Platinum lounge is located by Gate 54, we look forward to welcoming you!"
```
{% endcode %}

5. Your Journey should now look something like this:

<figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 13.06.44.png" alt=""><figcaption></figcaption></figure>

### Push Message - Check In

1. From the actions tab, choose **Push** and drag it after the Webhook along the `Bronze and Silver` path.
2.  Click on the activity to open the detailed view.

    1. Set the **label** to `Check in Push`.
    2. Set the **push category** to `Transactional`.
    3. Set the **push surface** to `Transactional_Email_Push`.
    4.  Click on **Edit content** to start designing your push message.

        1. Set the **title** to `Time to check in for your flight`.
        2. Click on the person icon next to the title input box to open the message editor. You can now select **profile attributes** for personalisation in the message. From the left menu, with profile attributes selected, search for `Latest Action`.
        3. Open the folder, look for `actionProduct` and click the + icon to add the personalised field to your expression. Your expression should read: `Time to check in for your flight {{profile._adobeamericaspot4.latestAction.actionProduct}}`
        4. Click**Save.**
        5. Set the **body** to `Check in 1 extra bag for free!`.
        6. Your screen should look like the image below. Navigate out of the designer by clicking the arrow on the top left of your screen.

        <figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 14.05.31.png" alt=""><figcaption></figcaption></figure>

    Your screen should look like the image below. Click **Ok**.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 14.06.31.png" alt=""><figcaption><p>Journey Creation - Push notification</p></figcaption></figure>

1. Repeat the same for the `gold` and `platinum` paths, adding push messages to those journeys with the **title** and **body** messages of your choice.

The journey is now finished. It should look like this:

<figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 14.13.00.png" alt=""><figcaption><p>The finished journey</p></figcaption></figure>
