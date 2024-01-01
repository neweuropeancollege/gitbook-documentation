## 2. Faulty Records Dashboard

This dashboard focuses on four reports that highlight potential data discrepancies for records that may apply to both applicants and partners.

### Auto-Refresh Configuration

**This dashboard is configured to auto-refresh every morning at 8 AM.**
- The auto-refresh ensures the data presented is up-to-date for the Admin's daily check.

### Reports and Information

1. **Bad Owner to User**
   - _Objective_: Correct ownership discrepancies in opportunity records.
   - _Resolution Steps_:
     - Align the 'User' picklist value with the 'Owner' field in opportunity records.
     - This issue mirrors the task mismatch in the General Overview Dashboard.

2. **Error Form Submissions**
   - _Objective_: Address form submission errors for proper conversion.
   - _Resolution Steps_:
     - Examine each error form submission for the reason behind the failure.
     - Correct the issue (e.g., often too long mailing city or postal code).
     - Change the status to 'New' and save to convert the form to an interaction.

3. **Bad Stage Before Close**
   - _Objective_: Ensure accurate tracking of opportunity closed stages.
   - _Resolution Steps_:
     - The 'Stage Before Close' field should differ from the current stage or be empty if not closed.
     - Correct any discrepancies to reflect the actual closed (or not) opportunity stages.

4. **No Account Report**
   - _Objective_: Link opportunities with an account.
   - _Resolution Steps_:
     - Update opportunities missing an associated account.
     - Ensure applicant opportunities are linked with administrative accounts, and agent opportunities with business organization accounts.