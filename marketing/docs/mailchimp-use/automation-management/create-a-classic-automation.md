# Create a Classic Automation

Introduction

This guide provides a comprehensive step-by-step process for creating and running a classic automation in MailChimp. It's crucial to understand that MailChimp refers to these as "classic automations," not campaigns. This distinction is important for effective utilization of the platform.

{% embed url="https://us10.admin.mailchimp.com/customer-journey/#/create-campaign/explore/emailCampaign:custom" fullWidth="false" %}
Create a Classic Automation
{% endembed %}

By using the design and configuring the settings as suggested here, Mailchimp will take care of moving an individual from one automation to another as their stage (or any other defined field on SF) changes, by way of the abstraction provided by the use of the _Exclusive Campaign Tracker_ model.

## Preliminary Steps

* **Determine the Automation Name**: Before initiating the process, decide on the automation's name, which should align with your automation objectives. Refer to \[\[List of Automation Names; their Structure, and their Segmentations|List-of-Automation-Names-their-Structure-and-their-Segmentations]] to find the name.
* **Decide on the Automation's Outcome**: Ascertain whether the automation will lead to the closure of SF opportunities and archiving in MailChimp. This is particularly relevant for automations targeting WOT prospects.
* **Choose Between Replicating or Creating New Automations**: Determine whether to replicate an existing automation (accessible from either the campaigns or automations tab) or to create a new one (only possible from the automations tab).

## Creating a New Classic Automation

1. **Navigate to the Automations Tab**: Start by selecting the Automations tab in MailChimp.
2. **Access Classic Automations**: Click on the "Checkout Classic Automations" link at the top center of the page.
3. **Select Automation Type**: In the "Create an Automation Email" section, go to the "Subscriber Activity" tab and choose "Respond to Subscriber Updates."
4. **Choose the Automation Trigger**: Click on "Audience Field Change" and select "Respond to Subscriber Updates." Enter the pre-decided automation name and choose "Everyone on Salesforce" as your audience.
5. **Configure Workflow Settings**:
   * **Workflow Name**: This becomes your automation name.
   * **From Name**: Use a general name like "New European College" to avoid multiple automations for different salespeople. The dynamic content will handle individual email signatures.
   * **From Email Address**: Use a general email like "admissions@new-european-college.com".
   * **Personalize the 'To' Field**: Check this option and specify the merge tag for re**cipient name**: |\*FULLNAME\*|
   * **Tracking Settings**: Leave the default settings for tracking opens, clicks, and Google Analytics link tracking. What goes into the Google Analytics Name field depends on what the Google Analytics Admin decides. E-commerce and Clicktail link tracking should be off. Note that Goal tracking and Salesforce stats are not available for classic automations.
6. **Setting Email Specifics in the Series**:
   * **Trigger for the First Email**: Ensure it's set to "Changes in a Subscriber's Audience Field" with the field being "Exclusive Campaign Tracker" and the condition being the name of your campaign.
   * **Scheduling**: Set to send emails every day at 6.45 PM Berlin time, considering Salesforce-Mailchimp synchronization schedules.
   * **Filter by Segment or Tag**: Set to "Contact Match the Following Conditions" with the condition being "Exclusive Campaign Trigger" is the automation name. This is what ensures the recipient still matches the conditions on the time of sending this email in the series. If not, they effectively exit out from the automation.
   * **Post-Send Action for the Last Email**: Set to "None" unless the automation is intended to close opportunities and archive contacts on Mailchimp. In such cases, configure the post-send action to update a merge field, the "To Be Archived" merge field, to "Yes" on the final email of the series. Then, the responsible person archives them on Mailchimp, sets MC Archived to ticked on Salesforce and closes their opportunity on Salesforce (if not done already).
7. **Configure Subsequent Emails in the Series**: For emails following the first, set the trigger to "Previous Email Sent" with a custom delay, usually some number of days. The delay and specific settings will depend on the objectives of your automation.

## Finalize and Start the Automation

Once all settings are configured, and email content is designed, proceed to start the automation. Ensure all steps are correctly set before initiating the sending process.

## Conclusion

By following these detailed steps, you can effectively create and manage classic automations in MailChimp, ensuring a seamless integration with Salesforce and Mailchimp. Remember to adjust settings according to the specific needs of your automation and organization.
