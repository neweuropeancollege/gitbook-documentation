# About the Integration Between MailChimp and Salesforce

## Overview
This document provides a high-level explanation of the integration between MailChimp and Salesforce, primarily using the MailChimp for Salesforce connector plugin. The aim is to simplify the understanding of the process for the reader.

## Key Integration Features

### Use of the MailChimp for Salesforce Connector Plugin
- The MailChimp for Salesforce connector plugin is used to integrate MailChimp and Salesforce.
- The plugin provides a two-way sync between MailChimp and Salesforce.
- Since Salesforce is the source of truth for contact information, the plugin is configured to sync data from Salesforce to MailChimp, however it does provide subscriber activity data back to Salesforce.

### Scheduled Processes
- A scheduled process occurs every 24 hours.
- During this process, a query is executed to select Contacts from Salesforce to transfer to MailChimp.

### Data Transfer to MailChimp
- The results of the Salesforce query are sent to MailChimp.
- In MailChimp, an audience with predefined merge fields exists.
- Salesforce query can define parameters for selecting Contacts.
- Fields from the Contact object in Salesforce can be mapped to the merge fields in MailChimp.
- This allows for the seamless transfer of contact information to MailChimp.

### Limitations in Field Types
- Certain field types from Salesforce, such as DateTime fields and Picklist fields, cannot be transferred to MailChimp due to connector limitations.
- These fields must be converted to Date and Text fields, respectively, in order to be transferred to MailChimp.

## Data Flow from MailChimp to Salesforce

### MC Subscriber Activities
- Activities of Contacts (MC subscribers) in MailChimp are represented in Salesforce as MC Subscriber Activity records.
- These records detail the type of activity (e.g., sent, click, open).
- The integration allows visibility into MailChimp activities within Salesforce.

### Visualization of Emails
- A trigger on the MC Subscriber Activity object in Salesforce:
  - Identifies records with the type 'sent'.
  - Calls the MailChimp API using the data to retrieve details like campaign sent, email content, and subject.
  - Creates an Email Message record related to the MC subscriber's associated Opportunity.

## Data Management and Source of Truth
- Salesforce serves as the single source of truth for contact information.
- New contacts are added to Salesforce and subsequently synced to MailChimp in the next scheduled query run.
- The query only considers records created or modified since the last run to optimize performance and avoid processing large batches.