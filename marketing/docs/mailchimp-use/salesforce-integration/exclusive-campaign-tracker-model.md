# The Exclusive Campaign Tracker Model in Salesforce

This documentation outlines the **Exclusive Campaign Tracker Model** used in Salesforce for determining which campaign or automation a contact should receive, with synchronization to MailChimp.

## Overview

The Exclusive Campaign Tracker Model in Salesforce is a method for deciding and tracking which campaigns (specifically automations in MailChimp terminology) a contact should receive. This process involves updating a specific merge field in MailChimp with the appropriate automation name, determined and sourced from Salesforce.

## Key Fields in Salesforce

There are three key fields in Salesforce related to this process:

1. **Exclusive Campaign Tracker Auto**: A formula field defining the default campaign for a contact based on predefined rules.
2. **Exclusive Campaign Tracker Manual**: A field for manual overrides of the campaign assignment.
3. **Exclusive Campaign Tracker**: A formula field that uses the value from `Exclusive Campaign Tracker Manual` if available, otherwise defaults to the value from `Exclusive Campaign Tracker Auto`.

## Process Workflow

1. **Determination of Campaign**:
   - The campaign a contact should receive is determined in Salesforce.
   - The decision is based on a formula that can utilize fields from the Contact object, related Account fields, and a subset of important fields from the contact’s latest Opportunity.

2. **Exclusive Campaign Tracker Field**:
   - This field integrates the decisions from both the auto and manual fields.
   - It serves as the central point for tracking the selected campaign for each contact.

3. **Synchronization with MailChimp**:
   - The value from the `Exclusive Campaign Tracker` field in Salesforce is synchronized with the corresponding contact's merge field in MailChimp.

4. **MailChimp Automations**:
   - Utilize the synchronized merge field from Salesforce to determine which automation/campaign a contact receives.

## Configuring Campaign Rules

- The campaign rules are set in the `Exclusive Campaign Tracker Auto` formula field.
- The configurator has access to:
  - All Contact fields
  - All Account fields
  - All fields from the Contact's Latest Opportunity (Latest_Opportunity__r)

## Conclusion

The Exclusive Campaign Tracker Model in Salesforce provides a flexible and robust mechanism to assign campaigns to contacts, allowing for both automated rule-based assignments and manual overrides. This model ensures seamless integration with MailChimp, enabling effective and targeted campaign automations.
