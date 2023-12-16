# Importing Missing Emails from Outlook to Salesforce

## Overview

We use Salesforce for some business operations such as student and agent recruitment, not all. Thus, not all email addresses are integrated to forward their incoming inbox messages to Salesforce for processing. In rare cases, it can happen that someone from another department receives an email that should be processed in Salesforce - e.g: if Sascha receives an email about student recruitment. These emails should be imported onto Salesforce. Here are the steps.

## Initial Setup on Outlook (you only have to do this once - the first time)

1. Navigate to Outlook (online or desktop)
2. Create a folder in your Outlook mailbox called 
```
REDIRECTNOWSF
```
* This folder should be in the uppermost position in the folder structure, in the same level as your inbox folder. **Don't create it within another folder!**
* Below is an example of a correct folder structure on Outlook to make this work:

![image](https://github.com/parsam97/nec-salesforce/assets/32430185/79a5a1bc-8513-4a3d-9a8b-4fa897eebb47)

## Importing the email

1. On Outlook, locate the email you wish to import in your inbox and drag it into the `REDIRECTNOWSF` folder
2. On Salesforce
   - Use the `Import Emails` utility, visible on the bottom right of any page.
   - Fill in your email address in the email field.
   - Click `Fetch emails`. If "Fetch emails" is greyed out, simply click anywhere on the utility window or click "TAB" on your keyboard.
   - Interaction records will be created for all emails in your `REDIRECTNOWSF` folder. The `Result` column will show a tick if import was a success.
   - You might get the message `Email already processed...` In this case, open the Email Header record by clicking the dropdown on the left and selecting the option to open. Then delete the entire Email Header record of the page which opens and try to Fetch Emails again.
   - The `Has attachments` will show a tick if any emails have attachments. To download their attachments into Salesforce as well (usually necessary if admission documents are present):
     - Click the menu-item downwards arrow on that email
     - Click `Download attachments`
   - The download process will be queued and attachments should show up on the interaction record after a minute or two depending on the size of the attachments.
   - To navigate directly to the interaction record created:
     - Click the menu-item downwards arrow on that email
     - Click `Open Interaction Record`
3. Back on Outlook
   - Remove the emails you dragged by dragging them back to your Inbox folder.

### Notes:

- Only the `REDIRECTNOWSF` folder is visible to the application
- The access and retrieval is done via `salesforcenec@new-european-college.com` account.
- You can enter the email address of anyone in our organization to fetch emails. The access is provided through the privileged account of `salesforcenec@new-european-college.com` and this account only has access to the contents of `REDIRECTNOWSF`. The receiving inbox need only to place the email into that folder and remove it after import.
