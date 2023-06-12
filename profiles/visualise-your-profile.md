---
description: >-
  In this exercise you will use the AEP UI to view your real-time customer
  profile.
---

# Visualise Your Profile

In Adobe's Real-time Customer Profile, all profile data is shown alongside event data, as well as existing segment memberships. The data shown can come from anywhere, from Adobe applications and external solutions. This is the most powerful view in Adobe Experience Platform, the true experience system of record.

## Use the Customer Profile View

{% hint style="info" %}
To log into the Adobe Experience Platform,[ go here](https://experience.adobe.com/#/@adobeamericaspot4/sname:uk-aep-bootcamp/platform/home).
{% endhint %}

1. In the left rail, click on **Profiles**.
2. On the **Profiles** tab, click on **Browse**.&#x20;

On the **Real Time Customer Profile** panel on the WKKND Fly website, you can find multiple identities. Every identity is linked to a namespace. You can see these combination of id and namespaces.

<table><thead><tr><th width="205.44090441932167">Identity</th><th>Namespace</th></tr></thead><tbody><tr><td><strong>EXPERIENCE CLOUD ID</strong></td><td><code>83433386964176742472712675204149950968</code></td></tr><tr><td><strong>EMAIL</strong></td><td><code>sacker+2004-1@adobetest.com</code></td></tr><tr><td><strong>PHONE NUMBER</strong></td><td><code>+447929141042+2004-1</code></td></tr><tr><td><strong>FREQUENT FLYER ID</strong></td><td><code>123124</code></td></tr></tbody></table>

With Adobe Experience Platform, all IDs are equally important. Previously, the Adobe ID was the most important ID in the Adobe context and all other IDs were linked to the ECID in a hierarchical relation. With AEP this is no longer the case, and every ID can be considered a primary identifier.

Typically, the primary identifier depends on the context.&#x20;

* If you ask your Call Center, "_What is the most important ID?",_ they will probably answer, "_the phone number!"._
* But if you ask your CRM team, they will answer, "_the email address!"._

Adobe Experience Platform understands this complexity and manages it for you. Every application, whether an Adobe application or non-Adobe application, will speak with Adobe Experience Platform by referring to the ID they consider primary. And it simply works!

1. For the field **Identity namespace**, select **Email** &#x20;
2. For the field **Identity Value** enter the email address you used for your flight booking in the previous exercise.&#x20;
3. Click **View**. You’ll then see your profile in the list.&#x20;
4. Click the **Profile ID** to open your profile.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 16.51.15.png" alt=""><figcaption><p>Profile Lookup</p></figcaption></figure>

You now see an overview of **Profile Attributes, Identities and Preferences** for your customer profile. This user interface is customisable.&#x20;

![Customer Profile Overview](../.gitbook/assets/profile\_view\_ridm.jpg)

If you’d like to see all available Profile Attributes for your profile,&#x20;

1. Click on **Attributes** at the tab bar of overview panel.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 16.53.35.png" alt=""><figcaption><p>Profile Attributes Details</p></figcaption></figure>

To see all entries for every experience event that is linked to your profile:

1. Click on **Events** at the tab bar.
2. You can click on **View all** for each event to see more details of a specific experience event.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 16.54.32.png" alt=""><figcaption><p>Experience Events</p></figcaption></figure>

To see all segments that this profile belongs to (we will discuss more about Segments in the next exercise):

1. Click on **Segment Membership** at the tab bar.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 16.55.41.png" alt=""><figcaption><p>Segment Memberships</p></figcaption></figure>

{% hint style="success" %}
You have now successfully viewed your customer profile in Adobe Experience Platform.
{% endhint %}

Now that you’ve learned how to view any customer’s real-time profile by making use of AEP’s User Interface, let’s create a segment which your profile will qualify for.&#x20;
