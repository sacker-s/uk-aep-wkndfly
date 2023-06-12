# Sharing Filters from CJA to CDP

This topic discusses how to create and publish audiences identified in Customer Journey Analytics (CJA) to Real-Time CDP (RTCDP) in Adobe Experience Platform for customer targeting and personalisation.

### Create audience <a href="#create" id="create"></a>

1.  To create audiences, you have three ways to get started:

    | Creation method                               | Details                                                                                                                                                                                              |
    | --------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | From the main **Components > Audiences** menu | The Audiences Manager page opens. Click **Create audience** and the Audience builder opens.                                                                                                          |
    | From within a Freeform table                  | Right-click an item in a Freeform table and select **Create an audience from selection**. Using this method pre-populates the filter with the dimension or dimension item you selected in the table. |
    | From the filter creation/editing UI           | Check the box that says **Create an audience from this filter**. Using this method pre-populates the filter.                                                                                         |
2. Build the audience of your choice with the method of your choice - for option 1 above, it would look like this:

<figure><img src="../.gitbook/assets/Screenshot 2023-04-26 at 08.31.38.png" alt=""><figcaption></figcaption></figure>

1. Interpret the data preview. The audience preview appears in the right rail. It allows for a summarised analysis of the audience you have created.
2.  Double-check your audience configuration and click **Publish**.

    If everything went well, you will receive a confirmation message that the audience was published. It takes only minute or two for this audience to show up in Experience Platform. (Even for audiences with millions of members, it should take less than 5 minutes.)

    1. Click **View audience in AEP** within the same message and you will be taken to the Segment UI in Adobe Experience Platform.&#x20;

### What happens after an audience is created? <a href="#after-audience-created" id="after-audience-created"></a>

After you have created an audience, Adobe creates an Experience Platform streaming segment for each new CJA audience. An AEP streaming segment will only be created if your organization is set up for streaming segmentation.

* The AEP segment shares the same name/description as the CJA audience, but the name will be appended with the CJA audience ID to ensure that it is unique.
* If the CJA audience name/description changes, the AEP segment name/description reflects that change as well.
* If a CJA audience is deleted by a user, the AEP segment is NOT deleted. The reason is that the CJA audience may later get undeleted.

### Use CJA audiences in Experience Platform <a href="#audiences-aep" id="audiences-aep"></a>

CJA takes all the namespace and ID combinations from your published audience and streams them into Real-time Customer Profile (RTCP). CJA sends the audience over to Experience Platform with the primary identity set, according to what was selected as the Person ID when the connection was configured.

RTCP then examines each namespace/ID combination and looks for a profile that it may be part of. A profile is basically a cluster of linked namespaces, IDs and devices. If it finds a profile, it will add the namespace and ID to the other IDs in this profile as a segment membership attribute. Now, for example, “user@adobe.com” can be targeted across all their devices and channels. If a profile is not found, a new one is created.

You can view CJA audiences in Platform by going to **Segments** > **Create segments** > **Audiences** tab - your CJA Audience will now be combined with the other segments in AEP.
