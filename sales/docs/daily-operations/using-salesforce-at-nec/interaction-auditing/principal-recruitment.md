# Principal Recruitment

This guide details the process for selecting the `Principal Recruitment` record type during the auditing of interactions, specifically when the interaction is **from an agent** about a **student's application**.

## Changing Record Type

1. **Accessing the Dialog Box**
   * Click on the `Change Record Type` button at the top right corner of the interface to open the dialog box.
2. **Selecting the Record Type**
   * In the dialog box, select the `Principal Recruitment` record type. This is relevant for interactions involving agents regarding student applications.

## Filling in the Fields

Upon selecting the `Principal Recruitment` record type, two sections will be presented: `The Student` and `The Agent`.

### The Student Section

After selecting the `Principal Recruitment` record type, you will encounter a section titled `The Student`, which includes fields such as:

* **Account**
* **Contact**
* **Opportunity**
* **Email** (mandatory)

#### Email Field Adjustment

In the `Principal Recruitment` process, it is essential to correctly update the `Email` field in the `The Student` section:

* **Initial Email Address**: The `Email` field initially contains the email address of the agent who is the sender of the interaction.
* **Required Change**: This email address must be replaced with the email address of the student who is the subject of the application.
* **Importance of Accuracy**: It is imperative to ensure that the email address in this field is that of the student. This adjustment is crucial for correctly associating the interaction with the student's record and not the agent's.
* **Finding the Student's Email**: If the student's email is not immediately known, it may be necessary to search for the student's contact record to locate the correct email address.
* **Updating the Email Field**: Once the student's email is identified, manually replace the agent's email with the student's in the `Email` field. This step ensures that all communication and records are correctly linked to the student's profile.

{% hint style="warning" %}
Failure to update the `Email` field with the student's email address can lead to miscommunication and incorrect data association in Salesforce.
{% endhint %}

#### Record Existence and Mandatory Fields

* `Account`, `Contact`, and `Opportunity` fields are mandatory **only if they exist in the system**.
* If these records exist for the student, they must be selected to avoid duplicates. If not, leave them empty.

### The Agent Section

This section is unique to Principal Recruitment and includes fields such as:

* **Affiliated Account**
* **Affiliated Contact**
* **Affiliation Role** (can be left empty)
* **Affiliation Status** (default set to current)

#### Filling Agent Fields

* **Affiliated Account**: Fill this with the agency's account record to which the agent belongs.
* **Affiliated Contact**: Insert the contact record of the agent who sent the interaction.

{% hint style="info" %}
Struggling to find the correct record among similar ones? Check out [these tips](../../learn-salesforce/finding-records-in-lookup-fields.md).
{% endhint %}

## Finalizing the Record Type Selection

* After verifying and correctly filling all fields in both the Student and Agent sections, click the `Change to Principal Recruitment` button at the bottom left of the dialog box.