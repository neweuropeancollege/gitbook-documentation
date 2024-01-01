## General Overview Dashboard

This dashboard consists of seven reports, each requiring specific actions for maintenance and data integrity.

### Auto-Refresh Configuration

**This dashboard requires manual refreshing to view the most current data.**
- The Admin must remember to manually refresh these dashboards each morning.
- This step is crucial as these dashboards do not update automatically due to org limitations on dashboard subscriptions.
- Consequence: Neglecting this step could result in reviewing stale data and missing new critical issues.

### Reports and Information

1. **Bounced Emails Last Month**
   - _Objective_: Identify and address bounced emails.
   - _Resolution Steps_:
     - Review the report for bounced emails.
     - Contact the responsible recruiter to resend or correct the email issue.

2. **Not Matching Tasks Assigned to User**
   - _Objective_: Align 'Assigned To' and 'User' fields in task records.
   - _Resolution Steps_:
     - Identify tasks with mismatched fields.
     - Manually update the 'User' picklist field to match the 'Assigned To' field.

3. **Email Addresses Not Processed - Last 2 Days**
   - _Objective_: Investigate and resolve issues with unprocessed emails.
   - _Resolution Steps_:
     - Identify emails that were not processed.
     - Determine if the issue is due to blacklisting or other errors.
     - Correct the underlying problem and attempt to reimport the email through Outlook.

4. **Today's Email Headers by Hour**
   - _Objective_: Monitor and ensure continuous email inflow.
   - _Resolution Steps_:
     - Observe the email traffic pattern.
     - Investigate any anomalies or gaps in email reception.

5. **Logins for Last 5 Days**
   - _Objective_: Track and verify user logins.
   - _Resolution Steps_:
     - Review the report to confirm expected user logins.
     - Follow up if necessary with users who have not logged in as expected.

6. **Subscriber Activity Imported as Activity**
   - _Objective_: Confirm successful import of MailChimp activities.
   - _Resolution Steps_:
     - Check for records marked as 'False' under 'Imported as Activity'.
     - Investigate and resolve any issues preventing successful import.
     - Note: the 'Unimported MC Emails' link provides a ListView to the same records. Further information below.

7. **Interaction Audit Report**
   - _Objective_: Ensure interactions are owned by active and correct users.
   - _Resolution Steps_:
     - Identify interactions owned by inactive or incorrect users.
     - Manually reassign these interactions to active users.
     - Confirm that the owner update is reflected in the system.