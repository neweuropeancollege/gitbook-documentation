# Daily Checks to be done Every Morning

## Introduction
This comprehensive guide is designed to assist the Salesforce Admin in conducting thorough daily checks using the Admin Dashboard. The dashboard features four key areas:
1. General Overview Dashboard
2. Faulty Records Dashboard
3. Faulty Applicant Records Dashboard
4. Faulty Partner Records Dashboard

Each section includes specific reports with detailed steps for resolution, ensuring that all aspects of the system function optimally.---
## 1. General Overview Dashboard
This dashboard consists of seven reports, each requiring specific actions for maintenance and data integrity.
### Detailed Report Analysis and Resolution
1. **Bounced Emails Last Month**  
- *Objective*: Identify and address bounced emails. 
- *Resolution Steps*:
- Review the report for bounced emails.
- Contact the responsible recruiter to resend or correct the email issue. 
2. **Not Matching Tasks Assigned to User**  
- *Objective*: Align 'Assigned To' and 'User' fields in task records. 
- *Resolution Steps*:
- Identify tasks with mismatched fields.
- Manually update the 'User' picklist field to match the 'Assigned To' field.
- Note: Only Admins have the rights to modify the 'User' field. 
3. **Email Addresses Not Processed - Last 2 Days**  
- *Objective*: Investigate and resolve issues with unprocessed emails. 
- *Resolution Steps*:
- Identify emails that were not processed.
- Determine if the issue is due to blacklisting or other errors.
- Correct the underlying problem and attempt to reimport the email. 
4. **Today's Email Headers by Hour**  
- *Objective*: Monitor and ensure continuous email inflow. 
- *Resolution Steps*:
- Observe the email traffic pattern.
- Investigate any anomalies or gaps in email reception. 
5. **Logins for Last 5 Days**  
- *Objective*: Track and verify user logins. 
- *Resolution Steps*:
- Review the report to confirm expected user logins.
- Follow up if necessary with users who have not logged in as expected. 
6. **Subscriber Activity Imported as Activity**  
- *Objective*: Confirm successful importation of MailChimp activities. 
- *Resolution Steps*:
- Check for records marked as 'False' under 'Imported as Activity'.
- Investigate and resolve any issues preventing successful import. 
7. **Interaction Audit Report**  
- *Objective*: Ensure interactions are owned by active and correct users. 
- *Resolution Steps*:
- Identify interactions owned by inactive or incorrect users.
- Manually reassign these interactions to active users.
- Confirm that the owner update is reflected in the system.---
## 2. Faulty Records Dashboard
This dashboard focuses on four reports that highlight potential data discrepancies.
### Detailed Report Analysis and Resolution
1. **Bad Owner to User**  
- *Objective*: Correct ownership discrepancies in opportunity records. 
- *Resolution Steps*:
- Align the 'User' picklist value with the 'Owner' field in opportunity records.
- This issue mirrors the task mismatch in the General Overview Dashboard. 
2. **Error Form Submissions**  
- *Objective*: Address form submission errors for proper conversion. 
- *Resolution Steps*:
- Examine each error form submission for the reason behind the failure.
- Correct the issue (e.g., incorrect mailing city or postal code).
- Change the status to 'New' and save to convert the form to an interaction. 
3. **Bad Stage Before Close**  
- *Objective*: Ensure accurate tracking of opportunity stages. 
- *Resolution Steps*:
- The 'Stage Before Close' field should differ from the current stage or be empty if not closed.
- Correct any discrepancies to reflect the appropriate stages. 
4. **No Account Report**  
- *Objective*: Link opportunities with the correct accounts. 
- *Resolution Steps*:
- Update opportunities missing an associated account.
- Ensure applicant opportunities are linked with applicant accounts, and agent opportunities with partner business accounts.---
## 3. Faulty Applicant Records Dashboard
Comprising six reports, this dashboard focuses on applicant record accuracy.
### Detailed Report Analysis and Resolution
1. **Student Ops No Contact**  
- *Objective*: Correct student opportunities without associated contacts. 
- *Resolution Steps*:
- Add missing contacts to student opportunities.
- Change misclassified records from student to agent opportunities where applicable. 
2. **Keystone/Integrator Opportunities**  
- *Objective*: Reassign improperly owned opportunities. 
- *Resolution Steps*:
- Reassign opportunities from Keystone and Integrator users to active sales users. 
3. **Student Ops Bad Account**  
- *Objective*: Correct account associations for student opportunities. 
- *Resolution Steps*:
- Ensure student opportunities are linked to administrative accounts.
- Modify incorrectly classified opportunities to partner opportunities if needed. 
4. **Bad Close Date**  
- *Objective*: Align close dates of opportunities with term start dates. 
- *Resolution Steps*:
- Verify that the close date matches the term start date.
- Adjust the close date accordingly, especially in cases of reopened opportunities. 
5. **Ops Ownership Spread**  
- *Objective*: Review distribution of student opportunity ownership. 
- *Resolution Steps*:
- Ensure correct user ownership of student opportunities. 
6. **Admin Accounts Ownership Spread**  
- *Objective*: Monitor administrative account ownership. 
- *Resolution Steps*:
- Confirm proper ownership of administrative accounts and rectify any mismatches.---
## 4. Faulty Partner Records Dashboard
This dashboard includes four reports emphasizing partner record correctness.
### Detailed Report Analysis and Resolution
1. **Bad Account**  
- *Objective*: Correct account types for partner opportunities. 
- *Resolution Steps*:
- Update incorrect account record types for partner opportunities.
- Reclassify opportunities to student/applicant types if necessary. 
2. **No NEC Affiliation**  
- *Objective*: Ensure NEC affiliation for partner contacts. 
- *Resolution Steps*:
- Verify and update NEC affiliations for contacts associated with partner opportunities.
- Create primary affiliations where missing and ensure correctness. 
3. **Partner Ops Ownership Spread**  
- *Objective*: Assess ownership distribution for partner opportunities. 
- *Resolution Steps*:
- Review and adjust ownership assignments for consistency and accuracy. 
4. **Business Accounts Ownership Spread**  
- *Objective*: Oversee ownership of business organization accounts. 
- *Resolution Steps*:
- Confirm and realign ownership of business accounts as necessary.---
## Additional Dashboard Operations
### Auto-Refresh and Manual Refresh
- Dashboards like Faulty Records and Faulty Applicant Records are auto-refreshed at 8 AM daily.
- General Overview and Faulty Partner Records Dashboards require manual refreshing for the latest data.
### Helpful Links Component
- Provides quick access to essential documents and records.
- Customizable for specific admin needs.---
## Conclusion
Daily checks are vital for a Salesforce Admin to maintain system health and ensure data accuracy. This detailed guide provides step-by-step instructions for resolving issues highlighted in the Admin Dashboard reports, thereby enhancing the overall efficiency of the Salesforce environment.
