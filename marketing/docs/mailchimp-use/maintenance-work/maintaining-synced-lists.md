# Maintaining Synced Lists Between Salesforce and MailChimp

## Introduction
This document outlines best practices and considerations for maintaining synchronized contact lists between Salesforce and MailChimp, focusing on the nuances of the MailChimp to Salesforce connector plugin and its interaction with Salesforce data.

## Key Considerations for Synchronization

### Modified Contacts Synchronization
- **Sync Trigger**: The MailChimp to Salesforce connector syncs only contacts modified since the last synchronization.
- **Typical Sync Frequency**: Synchronization usually occurs every 24 hours, affecting only records modified in this timeframe.

### Handling Formula Fields in Salesforce
- **Formula Field Limitation**: Formula fields updates do not alter the 'Last Modified Date' of a record, potentially causing sync issues.
- **Scenario Examples**:
  - _Configuration Changes_: Altering formula field configuration can change field values without updating the 'Last Modified Date'.
  - _Cross-Object Dependencies_: Formula fields depending on related records (e.g., account records linked to contacts) may update without changing the contact's 'Last Modified Date'.

### Resolution Strategies
- **Adjusting Member Queries**:
    - Navigate to the `MailChimp for Salesforce` app.
    - Navigate to the `MC Setup` tab > `Member Queries` section.
    - Use the `Schedule` option for the `Everyone on Salesforce` member query.
    - Set `Last Run Date` to a past date covering all desired contacts for synchronization.
    - Click `Save`.

### Deleted Contacts Synchronization
- **Deletion in Salesforce**: Contacts deleted in Salesforce are not automatically archived or deleted in MailChimp.
- **Impact**:
  - Potential discrepancies in contact counts between Salesforce and MailChimp.
  - Deleted Salesforce contacts may remain in MailChimp, leading to data inaccuracies.

### Manual Comparison and Cleanup
- **Weekly Comparisons**: Administrators should export and compare contact records from both Salesforce and MailChimp weekly.
- **Identification Process**: Use the `Contact ID` field to identify discrepancies between the databases.
- **Action Steps**: Decide whether to archive or permanently delete unmatched MailChimp contacts. Archiving is usually the way to go.

### Unsubscribed or Cleaned Contacts on MailChimp
- **Unsubscribe Scenario**: Contacts who unsubscribe on MailChimp will no longer receive updates.
- **Impact on Synchronization**: Unsubscribed contacts in MailChimp cease to update, leading to potential data mismatches. This is usually not a problem since the contact ceases to receive any emails from MailChimp, so the obsolete data on MailChimp is not a concern.

## Conclusion
Regular monitoring and proactive adjustments are crucial for maintaining accurate and synchronized contact lists between Salesforce and MailChimp. Understanding the limitations of the synchronization process and implementing systematic review procedures will ensure data integrity and consistency across platforms.
