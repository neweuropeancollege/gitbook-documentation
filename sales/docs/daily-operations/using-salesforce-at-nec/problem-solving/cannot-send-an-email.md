# An Email Can't Be Sent Due to an Error

When encountering an issue where an email can't be sent due to an error in Salesforce, it's essential to understand that this is likely a specific problem, as emails are generally sent successfully. Here's a step-by-step guide to troubleshoot this issue.

## Step 1: Verify Email Configuration

- Ensure that **email addresses** of the recipient Contact record are correctly configured.
- Check for any **recent changes** in the configuration that might have led to the issue.

## Step 2: Inspect the Contact or Opportunity

- Examine the **contact** or **opportunity record** you are trying to send an email to.
- Look for any **incorrect or missing values** that might be causing the error.

## Step 3: Analyze Previous Email Activities

- Confirm if this is **not the first attempt** to send an email to the account.
- If previous emails were sent successfully, identify **what has changed** since the last successful email.

## Step 4: Review Error Messages

- Carefully read the **error message** provided.
- Try to **deduce the cause** of the error related to recent activities or unique aspects of this specific opportunity or contact.

## Step 5: Check the Email Address Record

- Verify the **email address** on the contact record.
- Ensure it is **correctly entered** and marked as **primary**.
- Refer to the article on [why the email address record is vital](../general-workflow/importance-of-email-address-records.md) for further guidance.

## Step 6: Compare with Other Emails

- Attempt to **send an email to a different contact** to see if it goes through.
- If successful, it indicates an issue specific to the **original record** you were trying to email.

## Conclusion

If these steps do not resolve the issue, it's possible that the problem lies with external factors beyond immediate control. In such cases, patience and further investigation are required.

Remember, troubleshooting is often a process of elimination. Keep exploring different angles and refer to Salesforce documentation for additional support.

**Good luck!**