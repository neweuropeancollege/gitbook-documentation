# Sending Bulk Emails

This documentation provides a step-by-step guide on how to create and send list emails (bulk emails) in Salesforce.

## Overview
Salesforce enables the sending of bulk emails, referred to as list emails, to multiple recipients. This feature is useful for targeting contacts or leads through list views, campaigns, or individual campaign members. Choosing ot send a list email comes down to whether you would like to to send a marketing-style email (would be sent through Mailchimp) or a personal-style email (similar to individual Outlook emails).

## Steps to Create and Send a List Email

### 1. Navigate to List Emails Object Tab
- Access the **List Emails** object tab in Salesforce.

### 2. Selecting Recipients
- Recipients can be chosen from:
    - **Contact or Lead List View**: Create and save a list view with specific filters on the Contact object tab.
    - **Campaign**: Target campaign members by creating a campaign and a corresponding report with complex targeting filters.

### 3. Creating a Campaign for Targeted Recipients (if needed)
- If targeting is complex, create a campaign and a detailed report with Contacts as the object.
- Save and run the report, then add these contacts to the campaign as members, then reference that campaign in the list email creation.

### Understand Sending Limits
- Salesforce imposes a limit of **5000 emails per day** for list emails.

### 4. Creating the List Email
- Specify the email's subject, content, and recipients.
- Attach files and insert merge fields as needed.

### 5. Saving or Sending the Email
- Save the email as a draft, send it immediately, or schedule it for later via the pop-up dialog.

## Important Considerations
- Sending a list email will **not** display the email in the opportunity timeline of the contact.
- The 'Last Email Sent' field on the Opportunity object will **not** be updated for recipients.

## Conclusion
List emails in Salesforce offer a powerful way to reach multiple recipients efficiently. Be mindful of the daily limit and the type of email that best suits your audience.