# Create Connections

## Objectives <a href="#objectives" id="objectives"></a>

* Understand the Data Connection UI
* Bring Adobe Experience Platform data into CJA
* Understand Person ID and data stitching
* Learn the concept of data streaming in Customer Journey Analytics

## Connections

{% hint style="info" %}
Ensure you are logged in to the Adobe Experience Platform. \
See [Introduction](http://localhost:5000/o/AdHcQAEqgUNGWDrsYHDV/s/B7YcsI0AWnJpaEuaKMtH/ "mention"), section **Access** how to get access.
{% endhint %}

To go to Customer Journey Analytics within the sandbox environment:

1. Click on the product selector at the top right.
2. Select **Customer Journey Analytics**.

![Select Customer Journey Analytics](../.gitbook/assets/select\_cja.jpg)

You will see the Customer Journey Analytics project view.

Let's create our first connection.

1. Click Create New Connection.

You will see the Create Connection UI. To ensure you are in the right sandbox.

1. Use the picker to select the correct sandox.

Switching to the correct sandbox will ensure the available datasets will be updated accordingly.

The UI has three distinct area:

* On the left side you will find all available AEP datasets underneath **Select datasets**.
* In the middle, you'll find the drag and drop area for datasets you want to connect to, indicated by **Add datasets to configure connection**.
* On the right side you will find the stitching area, where you will select the **Person Id**.

## Select Datasets

We will now select datasets for our connection.

1. Search for the dataset **Demo System - Event Dataset for Website (Global v1.1)**.&#x20;
2. When selected click **+** to add dataset to the connection.
3. Search and when found select the checkbox in front of the following datsets:
   1. **Demo System - Event Dataset for Voice Assistants (Global v1.1)** and&#x20;
   2. **Demo System - Event Dataset for Call Center (Global v1.1)**.
4. Click on **Add** to add these datasets as well.

Your screen should now look like...

## Person ID and Data Stitching

Our goals in now to join these datasets. If you look on the right panel, you will see a field named Person ID. Each datasets has its own Person ID field. Check each dataset to see what is the Person ID.

As you will notice, most of them have the Person ID selected automatically. This is because a primary identifier is selected in every schema in Adobe Experience Platform. As an example, for  the schema for Demo System - Event Schema for Call Center (Global v1.1), the Primary Identifier is set to phoneNumber.

However, you can still influence which identifier will be used to stitch datasets together for your connection. You can use any identifier that is configured in the schema linked to your dataset.&#x20;

1. Click on the dropdown to explore the IDs available on each dataset.

As mentioned, we can set different Person IDs for each dataset. This allows you to bring different datasets from multiple origins together in CJA. Imagine bringing in NPS or survey data which would be very interesting and helpful to understand the context and why something has happened.

The name of the Person ID field isn’t important, as long as the value in the Person ID fields correspond. Let say we have email in one dataset and emailAddress in another dataset defined as Person ID. If delaigle@adobe.com is the same value for the Person ID-field on both datasets, CJA will be able to stitch the data.

### Stitching using Person ID

Now that you understand the concept of stitching datasets using the Person ID, let’s choose `email` as your Person ID for each dataset.

1. Select each dataset.
2. Select email from the Person ID dropdown list box.

Once you have stitched the three datasets, we are ready to continue.

1. Click on Next.

## Naming and Streaming

We now have to give our connection a name.

1. Enter _`identity`_` ``- Omnichannel Data Connection` in **Name** connection.
2. Enable **Automatically import new data for all datasets in this connection, beginning today** by switching the toggle to on.
3. Check **Import all existing data** and select `less than 1 million` from the **Average number of daily events**.

{% hint style="warning" %}
Do **not** click **Save**; we already have set up a connection for you.
{% endhint %}

After you have created your connection it may take a few hours before your data is available in CJA. That is why we will use a connection we defined already for you.

{% hint style="success" %}
You now have completed setting up a connection for CJA.
{% endhint %}



