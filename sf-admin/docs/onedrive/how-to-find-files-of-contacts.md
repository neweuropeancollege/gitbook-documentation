# How to Find Files of Contacts on Salesforce Linked to OneDrive

This documentation outlines the process for locating files associated with contacts in Salesforce, which are stored in OneDrive due to Salesforce's file storage limitations. It explains how to navigate Salesforce and OneDrive to access these files.

## Overview

Salesforce integrates with OneDrive for file storage. When files are submitted via forms or emails and matched with an existing Salesforce contact, they are automatically uploaded to a corresponding folder in the contact's account on OneDrive. Unmatched files remain in Salesforce until audited. Additionally, files sent via email are stored on the mail server, and those uploaded through Gravity Forms are on the website server.

## Finding Files Linked to Salesforce Accounts in OneDrive

### Steps to Locate Files on Salesforce

1. **Navigate to the Relevant Account Record:**
   - From the contact record in Salesforce, identify and navigate to the associated account record.

2. **Access OneDrive Files in the Related List:**
   - Scroll to the bottom of the account record page to find the 'Related' section.
   - Locate the 'OneDrive Files' related list. This list displays files associated with the account.

3. **Open OneDrive File Records:**
   - Each file record includes a URL link.
   - Click on the link to access the file directly in OneDrive.

### Locating Files Directly in OneDrive

1. **Obtain the Account ID from Salesforce URL:**
   - While on the account record page in Salesforce, observe the URL in the browser.
   - The Account ID is part of this URL. It typically follows the pattern `/lightning/r/Account/` and is a 15 or 18 character alphanumeric code.

2. **Use Account ID to Find Files in OneDrive:**
   - Navigate to the provided [OneDrive folder link](https://neweuropeancollege-my.sharepoint.com/personal/salesforcenec_new-european-college_com/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Fsalesforcenec%5Fnew%2Deuropean%2Dcollege%5Fcom%2FDocuments%2FSalesforce%20Files&view=0).
   - Search for a folder named with the Salesforce Account ID.
   - Review the files within this folder to find the ones related to the account.

## Important Notes

- **File Storage Locations:**
  - In addition to OneDrive, files are also stored in their source locations (mail server for emails, website server for Gravity Forms submissions).

- **Deleting Files:**
  - Deleting files from OneDrive removes them from the OneDrive system.
  - Deleting an account record in Salesforce does not delete associated files in OneDrive.
  - Files are typically deleted directly from the interaction page on Salesforce, which removes them from OneDrive.

- **Handling Account Records:**
  - Account records are generally not deleted. They are either merged or retained as is.

## Conclusion

This process provides a systematic approach to finding and managing files related to Salesforce contacts, stored in OneDrive.
