# Send your Segment to a Destination: Facebook

### Context

Activate profiles for your Facebook campaigns for audience targeting, personalisation, and suppression based on hashed emails.

You can use this destination for audience targeting across Facebook’s family of apps that are supported by Custom Audiences, including Facebook, Instagram, Audience Network, and Messenger. Selection of the app that you want to run campaign against is indicated at the placement level in Facebook Ads Manager.

{% hint style="info" %}
Facebook Custom Audiences supports the activation of identities:&#x20;

* GAID - Google Advertising ID
* IDFA - Apple ID for Advertisers
* phone\_sha256 - Phone numbers hashed with SHA256 algorithm
* email_lc_sha256 - Email addresses hashed with SHA256 algorithm
* extern\_id - Custom user IDs

**Export Type = Segment Export**
{% endhint %}

Facebook requires that no personally identifiable information (PII) is sent in clear. Therefore, the audiences activated to Facebook can be keyed off _hashed_ identifiers, such as email addresses or phone numbers.

### Activate Segments to the Facebook Destination

{% hint style="info" %}
To log into the Adobe Experience Platform,[ go here](https://experience.adobe.com/#/@adobeamericaspot4/sname:uk-aep-bootcamp/platform/home).
{% endhint %}

1. In the left menu, go to **Destinations**, then go to **Catalog**. You’ll then see the **Destinations Catalog**.
2. In **Destinations**, select **Social**, click the **Activate Segments** on the **Facebook Custom Audiences** card.

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 17.19.52.png" alt=""><figcaption><p>Destinations Catalog</p></figcaption></figure>

1. Select your Destination and click **Next**.

{% hint style="info" %}
For this Lab we have already configured the Facebook Destination for our demo account. You can reuse this Account to map your segments in the Lab:\
**Facebook Destination - UK Bootcamp**
{% endhint %}

In the list of available segments

1. Select the segment you created in the previous exercise.&#x20;
2. Click **Next**.

For the Facebook Custom Audience Destination, you need to specify your **mapping identifiers** between Adobe Experience Platform and Facebook. These will be used to match the profiles in your segments between platforms.

For this lab we want to use the `Hashed Email ID` as the mapping identifier.

1. On the **mapping** step select **Add new mapping**.
2. We will first specify a **Source Field,** by selecting the arrow next to the input box. This opens our XDM schema where we can choose to select from attributes or Identity namespaces.
3. Select the checkbox **Select identity namespace** and click the `Emails (SHA256, lowercased)` namespace from the list of identities.
4. Click **Select.**

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 17.25.42.png" alt=""><figcaption><p>Select Mapping field for Facebook Destination</p></figcaption></figure>

Then, we do the same for the **Target Field**.

1. Select the Hashed email ID (**email\_lc**_**\_**_**sha256)** from the Facebook options.&#x20;
2. Click **Select.**

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 17.28.19.png" alt=""><figcaption></figcaption></figure>

Your mapping should now look like:&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2023-04-19 at 17.29.09.png" alt=""><figcaption></figcaption></figure>

1. Click **Next.**&#x20;

On the **Segment Schedule** step,&#x20;

1. Select **Directly from customers** in the **Origin of Audience** drop down option.&#x20;
2. Click **Next**
3. Finally, on the **Review** page, click **Finish**.

{% hint style="success" %}
Your segment is now activated to Facebook
{% endhint %}

### Exported Data

For Facebook, a successful activation means that a Facebook custom audience would be created programmatically in [Facebook Ads Manager](https://www.facebook.com/adsmanager/manage/). Segment membership in the audience would be added and removed as users are qualified or disqualified for the activated segments.

{% hint style="info" %}
The integration between Adobe Experience Platform and Facebook supports historical audience backfills. All historical segment qualifications get sent to Facebook when you activate the segments to the destination.
{% endhint %}

## Context

Activate profiles for your Facebook campaigns for audience targeting, personalisation, and suppression based on hashed emails.

You can use this destination for audience targeting across Facebook’s family of apps that are supported by Custom Audiences, including Facebook, Instagram, Audience Network, and Messenger. Selection of the app that you want to run campaign against is indicated at the placement level in Facebook Ads Manager.

