## Overview

This article provides a detailed explanation of the significance of email records in Salesforce, particularly their relationship with contacts, and the implications of incorrect interaction auditing.

## Introduction

In Salesforce, managing contact information efficiently is crucial for maintaining accurate data and facilitating effective communication. The `Email Address` object plays a pivotal role in this context, as it allows for the storage of multiple email addresses associated with a single contact.

## Importance of Email Address Records

1. **Multiple Email Addresses**: Contacts can have numerous email addresses. This flexibility is essential for capturing all possible communication channels of a contact.
2. **Email Auditing**: When an interaction (such as an email) is received, Salesforce matches the interaction by matching the email address with the corresponding contact. This process is very relevant to the correct association between email addresses and contacts.

## Where to find Email Address Records

![emailaddresses_defaced](https://github.com/parsam97/nec-salesforce/assets/32430185/7fd0dfe8-b3e3-4c25-9d14-6bf81e10df09)

## Potential Issues and Solutions

1. **Incorrect Email Association**:
   - *Problem*: If an email address is incorrectly linked to a contact, any interactions from that email will be erroneously logged under the wrong contact, opportunity, or account.
   - *Solution*: It's vital to promptly correct such mistakes by updating the email address and **setting it to primary** in the contact's related list to reflect the correct association.

2. **Creation and Deletion of Email Records**:
   - *Action*: If an incorrect email address is associated with a contact, it can be deleted. Subsequently, when an interaction from the correct contact is audited, a new **primary** email address record will be created and correctly associated.
   - *Impact*: This ensures that future interactions are accurately logged and associated with the correct contact.

3. **Logging New Interactions**:
   - *Challenge*: If a contact’s email address is missing or incorrectly linked, logging new interactions can be problematic.
   - *Resolution*: Verify and rectify the **primary** email address records of the contact to enable accurate logging of interactions.

_Note: Primary Email Address records are marked with a **Primary** field on the Email Address record._

## Conclusion

Maintaining accurate email address records for contacts is essential for ensuring the correct logging of interactions and preserving the integrity of data within Salesforce. Regular audits and updates to these records are critical to avoid misinformation and data inconsistencies.
