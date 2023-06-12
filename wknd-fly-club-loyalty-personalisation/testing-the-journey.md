---
description: In this exercise we'll test the journey we've build.
---

# Testing the journey

In Adobe Journey Optimizer you can run journeys in test mode to test if the outcome of your journeys aligns with your requirements.&#x20;

To enable test mode, toggle **Test** on the top right of your journey.

While in test mode, you can not make changes to the journey. You'll also notice that the left menu is replaced with the Test mode panel.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-20 at 14.14.05.png" alt=""><figcaption><p>Journey Test Mode interface</p></figcaption></figure>



1. Click on **Trigger an event**. This will open a window. In this window you can choose a profile to be in the **Segment qualification** activity.
2. When we set up the Segment qualification, we chose Email as the main identifier. Enter your test profile's Email as the profile identifier and click **Send** to start the test.

{% hint style="warning" %}
If you want to receive the Push notification in your mobile app, you must be logged in with the same Email you use to trigger the test.

You will also need to make sure your profile is a member of the WKND Fly Club by signing up on the website if you haven't already.
{% endhint %}

The window will close and the test will now start. In a few moments you'll see more arrows turn green. This is your test profile moving through the journey. You will receive the push notification on your mobile device and a message posted to the Webhook within the next minute.&#x20;

{% hint style="info" %}
You can see the messages being posted to the Webhook here:&#x20;

[https://webhook.site/#!/bbba6759-2cdb-4320-8f4d-28f92e6c4872/2782f182-a82e-4735-8702-1882b3c44483/1](https://webhook.site/#!/bbba6759-2cdb-4320-8f4d-28f92e6c4872/2782f182-a82e-4735-8702-1882b3c44483/1)
{% endhint %}

{% hint style="success" %}
You've now tested your journey
{% endhint %}

1. Turn off test mode by toggling **Test**.
2. Click the **<** in the top left to navigate back to the **Journeys overview**.
