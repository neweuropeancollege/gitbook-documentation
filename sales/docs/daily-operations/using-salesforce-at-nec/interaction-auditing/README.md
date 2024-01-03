# Auditing interactions is a central responsibility of recruiters at NEC

## Overview
Prospective students interact with NEC, either through an email to any of our admission consultants, a form submission through any of our forms, a telephone call to our number, a visit to our campus, etc...

Each and every interaction that a prospective student makes with NEC  **is recorded in our Salesforce environment as an `interaction record`**. Part of your job as a recruiter is to  **audit these records** (specifically the ones assigned to you).

## Why audit interaction records

Auditing interaction records is a critical process in managing data within our organization. This practice ensures the accuracy, consistency, and reliability of data gathered from various sources. Here are some key reasons for auditing interaction records:

1. **Data Validation**: Interaction records often contain unstructured or semi-structured data. Auditing helps validate this data, ensuring it meets the organization's standards. For instance, people may enter their names in different formats (like using lowercase or mixing up first and last names). Auditing corrects these inconsistencies.

2. **Proofreading and Quality Control**: Even structured data can contain errors. Auditing enables the identification and correction of these inaccuracies. Incorrect information in fields like addresses can lead to communication barriers or operational inefficiencies.

3. **File Identification and Clarification**: In cases where files are submitted, although humans can understand the content, systems may not automatically recognize the file type or content. Auditing involves telling the system what the file is, making it understandable and usable within the organizational framework.

4. **Consolidation of Communication**: Interaction records consolidate various forms of communication – emails, form submissions, phone calls, in-person interactions, and event engagements – into a unified format. This consolidation provides a convenient way to manage and access all forms of communication in one place.

In conclusion, auditing interaction records is not just a matter of data organization but a crucial step in maintaining the integrity and usefulness of the information that flows into an organization. This process ensures that all types of incoming communication are accurately represented, understood, and utilized for effective decision-making.

5. **Rate the Sender**: Each interaction record gives an opportunity to assess the sender's credibility, reliability, and relevance. These ratings are crucial in understanding the sender's overall profile and potential impact on the organization.

By consolidating these individual ratings over time, we gain a comprehensive overview of each sender. This holistic view aids in:

  - **Prioritization**: Understanding the sender's rating helps in prioritizing responses and resources. Higher-rated interactions might be addressed more promptly or given more attention.
  - **Forecasting**: The cumulative rating can be used for forecasting and strategic planning, as it provides insights into the sender's potential future interactions and their significance.

Auditing interaction records is not just about maintaining data accuracy, but it also plays a strategic role in evaluating and leveraging sender information for organizational decision-making.

## What does Audit mean?

**The audit process**  is a process that intends to turn unstructured data into structured data. What does that mean? An email, for example, has information like name, phone number, country of origin, desired program, desired term, etc. The auditor needs to simply **read the email** and  **extract information** from the email onto the info's respective field on the `interaction record`.

- For example, if an email reads
> My name is Art Vandalay and I'm interested in your bachelor program starting next year February. I like to play basketball.

...your auditing job would be to:
1. find the **`first name`** field and fill it with **`Art`**
2. find the **`last name`** field and fill it with **`Vandalay`**
3. find the **`recruitment interest`** field and fill it with **`Bachelor`** (as you start typing Bachelor, the system will suggest you the Bachelor program)
4. find the **`term`** field and fill it with **`February 202x`** (similar to above, the system will suggest you the correct choice)
5. find the **`notes`** field and fill it with something helpful for yourself later like **`he loves to play basketball`** (you will see where this helps you later)

## How to do a Full and Complete Audit

1. First, navigate to the interaction record you wish to audit.
This is typically found by going to the Interaction object page, changing the list view to _My Interactions to Audit_ and starting from the bottom up as it is order by latest interaction at the top.
2. Before you do anything, you must ensure the  `Record Type`  of the interaction is set to the correct one. Please refer to the chart below to find the correct record type.


    * Selecting the correct record type requires you to provide the sender information. This is includes
        - `Account` field
        - `Contact` field
        - `Opportunity` field
        - `Email` field
        - `Last Name` field
        And maybe
        - `Affiliated Account` field
        - `Affiliated Contact` field

    * Please refer to the chart below to choose the correct record type, and complete the necessary steps for that record type before you continue.


3. Find the  **`Interaction Status`**  field and change the selection from Audit Required to  **`New`**
    * It's the first field, right at the top.
4. Find the fields  **`Rating of Intention`**  and  **`Quality of Communication`**  and provide them, judging the values solely based on the contents of the current interaction.
    * These fields are mandatory. That's so we can later rate the quality of the opportunity, and the likelihood of the opportunity to close successfully.
    * Providing a value for these rating fields will also allow you to **prioritize your work** later, an absolute must when work volume rises.
5. **Audit**  the interaction, as it was explained by the audit process above with Art Vandalay.
    * Remember, this part only requires you to extract info from the contents of this current interaction record. That means if you remember the prospect had informed you of something in an earlier interaction, it _does not_ need to be reiterated during this audit. That is also why you do not see the current data about the contact prefilled out on the interaction!
6. Specify whether you want the system to automatically create a  **task for you to follow up**  on this interaction. This is on by default for your convenience.
    * Find the  `Task Information`  section.
    * You may specify by when you want this task to be due (default _today_)
    * You may specify the priority of this interaction (default _Normal_)
    * You may specify additional comments to remind you as you complete the task (no need to repeat the interaction contents here, you can automatically see the interaction contents as you complete your task.)
7. Hit  **save**.
8. If the interaction came with files, transfer those files (documents) using the dialog window on the right. It is easier to show this visually. Ask someone if you think you need help.

## The Record Type of the Interaction Depends on its Sender!

Different kinds of interactions with our organization dictate the record type the interaction should have. Please use the information below to select the correct record type for the interaction you are auditing.