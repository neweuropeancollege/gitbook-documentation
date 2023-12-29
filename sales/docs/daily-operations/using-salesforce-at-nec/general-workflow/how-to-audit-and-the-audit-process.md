# How to Audit and the Audit Process

## Overview
Prospective students interact with NEC, either through an email to any of our admission consultants, a form submission through any of our forms, a telephone call to our number, a visit to our campus, etc...

Each and every interaction that a prospective student makes with NEC  **is recorded in our Salesforce environment as an `interaction record`**. Part of your job as a recruiter is to  **audit these records** (specifically the ones assigned to you).

## How to audit interaction records

1. First, navigate to the interaction record you wish to audit.
This is typically found by going to the Interaction object page, changing the list view to _My Interactions to Audit_ and starting from the bottom up as it is order by latest interaction at the top.

**The audit process**  is a process that intends to turn unstructured data into structured data. What does that mean? An email, for example, has information like name, phone number, country of origin, desired program, desired term, etc. The auditor needs to simply **read the email** and  **extract information** from the email onto the info's respective field on the `interaction record`.

- For example, if an email reads
> My name is Art Vandalay and I'm interested in your bachelor program starting next year February. I like to play basketball.

...your auditing job would be to:
1. find the **`first name`** field and fill it with **`Art`**
2. find the **`last name`** field and fill it with **`Vandalay`**
3. find the **`recruitment interest`** field and fill it with **`Bachelor`** (as you start typing Bachelor, the system will suggest you the Bachelor program)
4. find the **`term`** field and fill it with **`February 202x`** (similar to above, the system will suggest you the correct choice)
5. find the **`notes`** field and fill it with something helpful for yourself later like **`he loves to play basketball`** (you will see where this helps you later)

The audit process involves a couple other things, here's the full list of things to do for a **full and complete audit**

1. Find the  **`Interaction Status`**  field and change the selection from Audit Required to  **`New`**
    * It's the first field, right at the top.
2. Find the fields  **`Rating of Intention`**  and  **`Quality of Communication`**  and provide them, judging the values solely based on the contents of the current interaction.
    * These fields are not mandatory. That's because some interactions don't qualify a judgment on the prospect.
    * Providing a value for these rating fields will allow you to  **prioritize your work ** later, an absolute must when work volume rises.
3. **Audit**  the interaction, as it was explained by the audit process.
    * Remember, this part only requires you to extract info from the contents of this current interaction record. That means if you remember the prospect had informed you of something in an earlier interaction, it _does not_ need to be reiterated during this audit.
4. Specify whether you want the system to automatically create a  **task for you to follow up**  on this interaction. This is on by default for your convenience.
    * You may specify by when you want this task to be due (default _today_)
    * You may specify the priority of this interaction (default _Normal_)
    * You may specify additional comments to remind you as you complete the task (no need to repeat the interaction contents here, you can automatically see the interaction contents as you complete your task.)
5. Hit  **save**.
6. Transfer any documents if the interaction came with attachments. (Easier to show this visually, ask someone if you think you need help.)