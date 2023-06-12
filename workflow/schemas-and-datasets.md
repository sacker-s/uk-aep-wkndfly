# Schemas and Datasets

Before starting the CJA Workflow, don’t forget about base step, which is to understand the data that is available in Adobe Experience Platform.

**Garbage in, garbage out.** Remember? You must have a clear idea of what data is available and how the schemas in Adobe Experience Platform are configured. Understanding the data that is in Adobe Experience Platform will make things easier, not only on the data connection part, but also when building visualizations and doing analysis.

## Understand Schemas and Datasets

Let's explore our schemas and datasets.

{% hint style="info" %}
Ensure you are logged in to the Adobe Experience Platform. \
See [Introduction](http://localhost:5000/o/AdHcQAEqgUNGWDrsYHDV/s/B7YcsI0AWnJpaEuaKMtH/ "mention"), section **Access** how to get access.
{% endhint %}

1. Go to **Schemas** in the left rail and explore the following schemas.
2. Click on the **Browse** tab.
3. Explore the following schemas:
   1. **Demo System - Event Schema for Website (Global v1.1)**.
   2. **Demo System - Event Schema for Call Center (Global v1.1)**.
   3. **Demo System - Event Schema for Voice Assistants (Global v1.1)**.
   4. Make sure you check at least things like&#x20;
      1. Identies. **CRMID**, **phoneNumber**, **ECID**, **email**. \
         Which identities are the primary identifiers, which ones are the secondary identifiers? \
         You can find the identifiers by opening a schema and looking at the object **\_experienceplatform.identification.core**. \
         Have for example a look at the schema [Demo System - Event Schema for Website (Global v1.1)](https://experience.adobe.com/#/@adobeamericaspot4/sname:sandbox01/platform/schema/browse/https%3A%2F%2Fns.adobe.com%2Fadobeamericaspot4%2Fschemas%2Fd9b88a044ad96154637965a97ed63c7b20bdf2ab3b4f642e).
      2. the commerce object inside the schema [Demo System - Event Schema for Website (Global v1.1)](https://experience.adobe.com/#/@adobeamericaspot4/sname:sandbox01/platform/schema/browse/https%3A%2F%2Fns.adobe.com%2Fadobeamericaspot4%2Fschemas%2Fd9b88a044ad96154637965a97ed63c7b20bdf2ab3b4f642e).
4. Preview the following datasets:&#x20;
   1. **Demo System - Event Dataset for Website (Global v1.1)**.
   2. **Demo System - Event Dataset for Call Center (Global v1.1)**.
   3. **Demo System - Event Dataset for Voice Assistants (Global v1.1)**.

![Explore the schema](../.gitbook/assets/event\_schema.jpg)
