# Adding New Contacts

## Overview

This article outlines the method for adding new contacts to Salesforce, particularly those not classified as prospective applicants or partners. This includes high school counselors, university lecturers, friends of the organization, and parents of students or applicants. We will discuss how to create these contacts and associate them with the right affiliations and roles.

## Determining Contact Type

Before adding a new contact, determine whether they represent a private individual or are part of an organization.

- **Private Individual**: Directly create the contact. A corresponding administrative account record is automatically generated.
- **Organization Member**: Create the organization's account first, then the contact. This is crucial for roles like high school counselors.

## Creating a New Contact

1. Navigate to the Salesforce Contacts section.
2. Select **New Contact**.
3. Enter necessary details, considering the contact type:
   - For private individuals, standard contact fields are sufficient.
   - For organization members, ensure the organization account is linked.

## Setting Up Affiliations

1. In the Contact record, go to the **Affiliations** related list.
2. Select **New Affiliation**.
3. Fill in details:
    - **Status**: Typically 'Current'.
    - **Role**: Define the role (e.g., 'Friend', 'Lecturer').
    - **Primary** mark the affiliation as primary.

## Synchronizing with MailChimp

- The primary affiliation syncs to a field called **MC NEC Status** on the Contact record.
- The MC NEC status (e.g., 'Current Friend', 'Current Business Partner') is used to segment contacts in MailChimp.

## Conclusion

This method streamlines adding diverse contact types, ensuring proper categorization and efficient MailChimp synchronization for targeted communication.
