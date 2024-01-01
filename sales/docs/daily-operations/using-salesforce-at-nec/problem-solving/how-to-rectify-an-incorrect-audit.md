# How to Rectify an Incorrect Audit

## Definition of Incorrect Audit

An incorrect audit occurs when:

- An interaction enters the system.
- The system tries to identify the sender via email address and phone number.
- A match is found, linking the interaction with a contact, opportunity, and account. However, the matched contact is incorrect.
- The incorrectly matched interaction gets audited and the incorrectly matched contact's, opportunity's, and account's data gets overwritten. The previous data is lost.

## Common Causes of Incorrect Audits

- Often occur between applicants and their relatives (e.g., siblings, uncles).
- More severe when happening between applicants.

## Consequences of Incorrect Audits

- Overwriting of correct contact data.
- Loss of critical information.
- Attachments stored under wrong contact records in Salesforce and file storage systems (e.g., OneDrive).

## Immediate Actions When Attachments are Involved

- Cease all Salesforce operations related to the affected contacts.
- Avoid responding via Salesforce; use Outlook if necessary.
- Consult a manager or qualified developer.

## Steps to Rectify an Incorrect Audit

### Stage 1: Reverting Changes

1. **Identify Incorrectly Related Records**
   - Navigate to the affected contact, account, and opportunity (the incorrectly matched ones).

2. **Revert Changes**
   - Manually revert any changes made due to the incorrect audit. 
   - Look at the information that was present in the interaction.
   - Find those data in the contact, account, and opportunity records and revert them to their previous state.
   - The history of some fields are tracked, but not all. Go to the chatter tab of the record to hopefully find the previous value.

### Stage 2: Re-auditing Interaction

1. **Preparation for Re-audit**
   - Clear the associated account, contact, and opportunity from the interaction record.
   - Ensure the email and phone number that caused the incorrect match are corrected.
   - Delete any activity and task records created due to the incorrect audit.
    - Navigate to the incorrectly related contact and opportunity.
    - Look for activity and task records linked to the incorrect audit.
        - Activity records could include email messages on the activity timeline (if the interaction was an email) or events (if the interaction was a form submission).
    - Carefully delete these records to ensure no trace of the incorrect audit remains.
        - This step is crucial to avoid confusion and maintain data integrity.

{% hint style="info" %}
For more information on this step, refer to the following [article](resolving-missing-emails-and-tasks-on-opportunities-activity-timeline.md).
{% endhint %}

2. **Re-auditing Process**
   - Re-audit the interaction.
   - If correct records exist, manually associate them during the audit.
   - If not, leave them empty for automatic creation.

3. **Finalizing the Audit**
   - Before saving, scroll to the bottom of the interaction record page.
   - Uncheck two checkboxes: 'Imported as Task' and 'Imported as Activity'. This will let the processor know that it should create activity and task records (this time going to the correct contact and opportunity).
   - Complete the audit process.

## Additional Considerations

- Ensure to check the importance of email address records in the related article.
{% content-ref url="../general-workflow/importance-of-email-address-records.md" %}
[importance-of-email-address-records.md](../general-workflow/importance-of-email-address-records.md)
{% endcontent-ref %}
