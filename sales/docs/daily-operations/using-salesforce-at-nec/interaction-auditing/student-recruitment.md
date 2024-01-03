# Student Recruitment

This guide provides a detailed overview of the process involved in selecting the `Student Recruitment` record type during the auditing of interactions.

Remember, this record type is used only when the interaction is **from a prospective applicant** and is **about their inquiry or application** to NEC.

## Changing Record Type

1. **Accessing the Dialog Box**
   * Click on the `Change Record Type` button at the top right corner of the interface to open the dialog box.
2. **Selecting the Record Type**
   * Within the dialog box, select the `Student Recruitment` record type. This is applicable when handling interactions related to inquiries or applications from prospective NEC students.

## Filling in the Fields

After selecting the `Student Recruitment` record type, you will encounter a section titled `The Student`, which includes fields such as:

* **Account**
* **Contact**
* **Opportunity**
* **Email** (mandatory)

### Email Field

* The `Email` field should be populated with the email address of the prospective student or applicant.

### Mandatory Fields

* While the `Email` field is always mandatory, the `Account`, `Contact`, and `Opportunity` fields are mandatory **only if they exist in the system**.

### Record Existence

* If the `Contact` record exists, then the `Account` record definitely exists. The same is true in reverse.
* In cases where `Account` and `Contact` exist, it is highly likely that an `Opportunity` also exists. Always verify to avoid missing existing records.
* **Important**: It is crucial to ensure that if these records exist, they must be selected to avoid creating duplicates and additional work.

### Typing and Selecting Records

* For the `Account`, `Contact`, and `Opportunity` fields, we are looking for the sender's account, contact, and opportunity records.
* If whichever of these records do not exist, leave them empty. The interaction processor will create the account, contact, and opportunity for you, when left empty.
* If they do exist, type in the respective search fields to find and select the correct records.

{% hint style="info" %}
Struggling to find the correct record among similar ones? Here are [ways to make it easier](../../learn-salesforce/finding-records-in-lookup-fields.md).
{% endhint %}

## Finalizing the Record Type Selection

* With all necessary fields verified and correctly filled, click the `Change to Student Recruitment` button at the bottom left of the dialog box to complete the process.
