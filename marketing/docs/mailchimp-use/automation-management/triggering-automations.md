# How to Make Automations get Triggered by Salesforce

## Introduction
This document explains how to use Salesforce data to trigger email automations in MailChimp.

## Overview
Salesforce, a customer relationship management tool, is used to store information about individuals, including their email addresses. This information is automatically transferred (synchronized) to MailChimp, a platform for sending email automations, every day at 6 p.m.

## Key Terms
- **Salesforce**: Where we store data about individuals (and everything else regarding recruitment).
- **MailChimp**: Where we send emails to these individuals.
- **Synchronization**: The process of updating MailChimp with the latest data from Salesforce.
- **Campaign Tracker**: A special field in Salesforce that helps us decide which email campaign a person should receive in MailChimp. For more, see [[The Exclusive Campaign Tracker Model and How It Works|The-Exclusive-Campaign-Tracker-Model-and-How-It-Works]].

## Data Synchronization
Each day, at 6 p.m., information from Salesforce is updated in MailChimp. The data sent from Salesforce to Mailchimp are **Contact Records**. Data such as:
- Name, email address, and other contact-related information.
- The stage the applicant is in, and other opportunity information, related to the **Contact record**.
- The 'Campaign Tracker' value (under the **Contact record**), which is crucial for deciding the email campaign they should receive.

## Triggering Automations in MailChimp
Once the data is in MailChimp, email automations are triggered based on the 'Campaign Tracker' value. This process involves two main steps:
1. **Segmenting in Salesforce**: In Salesforce, admins will initially define how to individuals get segmented (e.g., based on their contact or opportunity details - as you wish) and set the appropriate 'Campaign Tracker' value for each desired segmentation. This is done on the backend [in setup](https://nec.lightning.force.com/lightning/setup/ObjectManager/Contact/FieldsAndRelationships/00NOj0000001X1x/view) and [by an admin](https://help.salesforce.com/s/articleView?id=sf.customize_formulas.htm&type=5) ONCE, and documented on [[List of Automation Names; their Structure, and their Segmentations|List-of-Automation-Names-their-Structure-and-their-Segmentations]].


<!-- Provide link and screenshot -->
<!-- You have to refer to Salesforce How to documentation - I will link -->


2. **Creating Automations in MailChimp**: Then on Mailchimp, you create an email campaign in MailChimp and set it to target individuals based on their 'Campaign Tracker' value, which comes from Salesforce.
We are currently able to segment based on the following opportunity data:
    * Cancellation Reason
    * Close Date
    * Closed Lost
    * Closed Won
    * First Intrc Author
    * Has Latest Opportunity
    * Is Closed
    * Is Won
    * Next Deadline
    * Next Target
    * Owner Name
    * Parent Stage
    * Plan Label
    * Plan Name
    * PStage Before Close
    * Record Type
    * Specialization Name
    * Stage Before Close
    * Stage Index [[Map of Opportunity Stage to Index|Map-of-Opportunity-Stage-to-Index]]
    * Stage Name
    * Term Name
    * Term Start Date
... and all contact and account (business, institiution, etc.) data.

For step-by-step instructions on setting up and running an automation on Mailchimp, see [[the guide|Mailchimp-Step-by-Step-Guide-Creating-and-Running-a-Classic-Automation]].

## Summary
To ensure effective email campaign targeting:
- Ensure Salesforce data, especially the 'Campaign Tracker' field, is accurately set based on individual segmentation.
- Synchronize Salesforce data with MailChimp daily.
- In MailChimp, create automations targeting the 'Campaign Tracker' values.
- Remember, the effectiveness of your email automations in MailChimp largely depends on the accuracy and timeliness of the Salesforce data you use.
