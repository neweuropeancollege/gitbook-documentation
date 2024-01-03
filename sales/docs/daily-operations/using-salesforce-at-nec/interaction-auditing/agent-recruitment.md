# Agent Recruitment

This guide outlines the process for selecting the `Agent Recruitment` record type during the auditing of interactions, specifically tailored for interactions related to the recruitment of agents.

## Changing Record Type

1. **Accessing the Dialog Box**
   * Click on the `Change Record Type` button located at the top right corner of the interface to open the dialog box.
2. **Selecting the Record Type**
   * Within the dialog box, choose the `Agent Recruitment` record type. This selection is appropriate for interactions that are centered around the recruitment of agents.

## Filling in the Fields

Upon selecting the `Agent Recruitment` record type, a section titled `The Agent` will appear with the following fields:

* **Account**
* **Contact**
* **Lead** (Always leave this field empty)
* **Opportunity**
* **Email**

### Field Details

#### Account Field

* Fill in the `Account` field with the agent's business organization account record if it exists in the system.
* If no relevant account record exists, leave this field empty.

#### Contact Field

* Populate the `Contact` field with the agent's contact record if available.
* Leave this field empty if there is no existing contact record for the agent.

#### Opportunity Field

* The `Opportunity` field should be completed with the agent's opportunity record if such a record exists.
* In the absence of an existing opportunity record, this field should be left blank.

#### Email Field

* The `Email` field should contain the email address of the agent.
* This field is essential for ensuring communication and records are correctly linked to the agent's profile.

### Mandatory Fields

* While the `Email` field is always mandatory, the `Account`, `Contact`, and `Opportunity` fields are mandatory **only if they exist in the system**.
* It is critical to ensure that if these records exist, they are selected to avoid the creation of duplicate records and additional work.

{% hint style="info" %}
Struggling to find the correct record among similar ones? Check out [these tips](../../learn-salesforce/finding-records-in-lookup-fields.md).
{% endhint %}

## Finalizing the Record Type Selection

* After ensuring that all necessary fields are accurately completed, click on the `Change to Agent Recruitment` button at the bottom left of the dialog box.