---
description: >-
  This section describes a typical user journey in the context of Adobe's
  real-time customer profile.
---

# Visit the WKND Fly Website

The journey from unknown to known is one of the most important topics amongst brands these days, as is the customer journey from acquisition to retention.

Adobe Experience Platform (AEP) plays a huge role in this journey. AEP is the brains for communication, the “experience system of record.”

AEP is an environment in which the word customer is broader than just the known customers. An unknown visitor on the website is also a customer from AEP's perspective and as such, all of the behaviour as an unknown visitor is also sent to AEP. Thanks to that approach, when this visitor eventually becomes (identified as) a known customer, a brand can visualise what happened before that moment as well. This helps from an attribution and experience optimisation perspective.

## Customer Journey Flow

{% hint style="info" %}
Access the [WKND Fly website here](https://dsn.adobe.com/web/sacker-KSDY?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6ImFub255bW91cyIsImVtYWlsIjoiYW5vbnltb3VzQGFkb2JlLmNvbSIsImlzc3VlciI6InNoYXJlZC1saW5rIiwiYXJnb24iOnsiYWNjZXNzIjoicmVhZC1wcm9qZWN0IiwicHJvamVjdElkIjoic2Fja2VyLUtTRFkifSwiaWF0IjoxNjgxOTE1MDk1LCJleHAiOjE2ODM3Mjk0OTV9.gpUzRgNByxuJqpNnW2eyD42kJGldmdKTtRSlV-FLeZo).
{% endhint %}

To go through the customer journey flow:

On the WKND Fly homepage, and any other page, you can get access to the **Real Time Customer Profile** panel.

* Click the Adobe logo icon on the top left corner of your screen to open the **Real Time Customer Profile** panel.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 15.40.30.png" alt=""><figcaption><p>WKND Fly Homepage with Real Time Customer Profile Panel</p></figcaption></figure>

* Have a look at the panel.
  1. Notice the **EXPERIENCE CLOUD ID** within **IDENTITIES**. This is the so-called Experience Cloud ID (aka ECID).
  2. Click on **ATTRIBUTES** to see all details (none, at the moment...) of this currently unknown customer.
  3. Click on **Events** to see the experience events that were collected based on the customer’s behaviour. The list is currently empty but that will change soon.

Let's behave as a typical customer now, we will search for our next flight

1. In the **Flight Search widget** above the homepage banner, search for a flight from **LHR** (London Heathrow) to **AMS** (Amsterdam).
2. Click on **Select** for the flight of your choice to proceed to the booking step.

You’ll then see the trip summary page for your chosen flight. Experience events of type **Flight Search** and **Flight Selection** have been sent to AEP. To inspect this event:

1. Open the **Real Time Customer Profile** panel.
2. Take a look at the **Events**.

You will see the interactions you have had with the WKND Fly web site.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 16.28.50.png" alt=""><figcaption><p>Website interactions as Experience Events</p></figcaption></figure>

While the behaviour is anonymous, we’re able to track every click and store it in Adobe Experience Platform. Once the anonymous customer becomes known, we will be able to merge all anonymous behaviour automatically to the known profile.

We will now continue with our flight booking where we will provide more information to WKND Fly and become a known customer:

1. From the Trip Summary page, fill in the form with your **preferences** and **passenger information**.

{% hint style="info" %}
If you would like to receive the emails in the following labs, fill in the passenger information email field with your email address.
{% endhint %}

{% hint style="warning" %}
Do not input any genuine card details into the **Payment Method** fields, you can leave these fields empty.
{% endhint %}

1. Click on **Confirm Purchase**. You have now booked a flight ticket and have become a known customer.
2. Refresh your browser.
3. Open the **Real Time Customer Profile** panel. You will see potential additional identities displayed, like your email address.
4. Click on **Attributes**. You will see additional profile details, like **NAME**, **PREFERRED MEAL**, **LATEST TRIP,** etc.
5. Click on **Events**. You’ll see all products that you viewed before.  All these (initially anonymous) events are now also connected to your new created profile.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 16.43.52.png" alt=""><figcaption><p>Profile Attributes and Identities</p></figcaption></figure>

You’ve now effectively seen a real-time, customer profile being created, first anonymous, then as a known profile, and continuously being enriched with experience events.&#x20;

In the next exercise, you’ll go ahead and visualise your profile in Adobe Experience Platform.
