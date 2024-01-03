# Other

This documentation outlines the procedure for selecting the `Other` record type during the auditing of interactions, specifically for cases where the interaction does not fit the usual categories of student or agent recruitment.

## Record Type Selection Criteria

* `Other` is selected when:
  * The interaction is not from a prospective student or an agent.
  * The initiator is not applying for themselves or representing an agency.
  * The interaction involves a third party (e.g., a family member or friend) acting on behalf of a prospective applicant.
  * The interaction's nature is outside the scope of student or agent recruitment but still requires documentation in Salesforce.

## Changing Record Type

1. **Accessing the Dialog Box**
   * Click the `Change Record Type` button at the top right corner of the interface to open the dialog box.
2. **Selecting the Record Type**
   * Choose `Other` from the options in the dialog box. This is used for interactions that do not fit any of the other interaction record types.

## Filling in the Fields

Upon selecting `Other`, a section titled `The Initiator of This Interaction` will be displayed with the following fields:

* **Account**
* **Contact**
* **Email**

### Field Details

#### Account and Contact Fields

* Typically, the `Account` and `Contact` fields are left empty, as interactions under `Other` often involve individuals not already present in the system.
* Fill these fields **only if** the initiator exists in the system.

#### Email Field

* The `Email` field should already be populated with the email address of the initiator.
* This field is critical for establishing communication and record linkage with the initiator.

### Processing Non-Applicant Interactions

* For interactions initiated by someone other than the applicant (like a parent or friend), the following steps are taken:
  * Process the interaction as `Other` and create an account and contact for the initiator.
  * Respond to the initiator, requesting the applicant's personal communication for further processing.
  * Instruct the initiator to declare their intent to act on behalf of the applicant, providing the applicant's full name and personal email address.
  * If such a declaration is received, that interaction is then processed under `Student Recruitment`, with the applicant's details replacing the initiator's in the relevant fields. In that interaction's audit, the `Account` and `Contact` fields will be left empty, so as to not overwrite the initiator's account and contact records.

### Special Considerations

* Typically, when selecting `Other`, the account and contact fields are left empty to facilitate the creation of a new record for the initiator.
* This approach addresses the frequent occurrences of third-party inquiries and helps maintain clarity and order within the Salesforce system.

## Finalizing the Record Type Selection

* After correctly filling the necessary fields, click on the `Change to Other` button at the bottom left of the dialog box.

{% hint style="info" %}
Processing an interaction under `Other` creates a contact whose relationship to our organization is not explictly defined. To define this (ensuring correct marketing segmentation "Friend of NEC"), create an affiliation for the contact. Refer to this article for [instructions on creating affiliations](https://app.gitbook.com/s/X9wDLmtb04bI08Wb87zk/general/adding-new-contacts#setting-up-affiliations).
{% endhint %}

***

This comprehensive guide is designed to ensure accurate and efficient handling of interactions under the `Other` category, which often involves third-party communications.
