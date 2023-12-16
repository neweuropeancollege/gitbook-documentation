# How to Create and Manage Programs

# Overview of the Plan Object in Salesforce

The Plan `Plan__c` object in Salesforce is utilized to manage both recruitment and academic aspects of our offerings. It's pivotal to understand the distinction between the two record types within the Plan object: Recruitment Plans and Academic Plans.

## Recruitment Plans
* These represent the marketing offerings displayed on our website for new applicants.
* Example: Bachelor of Business Administration (BBA) as a showcased program.
## Academic Plans
* These are the actual programs in which applicants enroll.
* Example Academic Plans: BBA, BBA+1, BBA+2.

# Linkages Between Recruitment and Academic Plans
* Recruitment to Academic Plan Linkage:
* Bachelor of Business Administration (BBA) => BBA

## Academic to Recruitment Plan Linkage:
* BBA => Bachelor of Business Administration (BBA)
* BBA+1 => Bachelor of Business Administration (BBA)
* MBM+1 => Master of Business Management (MBM)

## Applicant Assignment Process:
Applicants initially apply to a Recruitment Plan. They are initially assigned to the default Academic Plan linked to that Recruitment Plan, changed later on the application’s opportunity record page based on their qualifications.

# Required Fields and Lookup Filters
When creating or editing records in the Plan object, it is essential to respect the lookup filters and accurately fill the required fields.

## Common Required Fields:
* Type__c: Distinguishes between Recruitment and Academic records.
* Active__c: Indicates whether the plan is currently active.

## Lookup Fields and Filters:
* Every lookup field in the Plan object has a specific filter that must be respected to maintain data integrity.
* Example: Academic_Program__c should be linked to an Account of type 'Academic Program'. This filter is enforced by the system, so you cannot make a mistake. However, you can still mistakenly lookup to the wrong ‘Academic Program’ record.

# Distinction Between Recruitment and Academic Plans in Our Records
This is a reiteration of the above concepts based on actual existing records in our org database.

## Recruitment Plans:
* Include programs like Bachelor of Business Administration (BBA), Master of Business Management (MBM), etc.
* These are the plans showcased to potential applicants.
* Each Recruitment Plan has a default Academic Plan linked to it. This linkage is crucial for automatically assigning an Academic Plan when an applicant shows interest in a Recruitment Plan.

## Academic Plans:
* Include specific programs like BBA, BBA+1, MBM, etc.
* These plans are assigned based on the qualifications of the applicants.
* Each Academic Plan is linked to the associated marketed Recruitment Plan. This is one way the system knows which Academic Plan belongs to which Program.

***

# Creating and Managing Plan Records

Creating or managing new Plan records in Salesforce requires following a specific order of operations. This process ensures that all necessary relationships and references are established correctly.

## Order of Operations

1. Confirm or Create the Educational Institution Account:
    * Check if the educational institution (Account record type: Educational Institution) exists in the system.
    * If it doesn't exist, create a new Educational Institution Account.
2. Confirm or Create the Academic Program Account:
    * Verify if the Academic Program (Account record type: Academic Program) related to the plan exists.
    * If not, create the Academic Program Account.
    * Use the 'Parent Account' field on the Account object to link the Academic Program to the Educational Institution.
3. Proceed to the Plan Object:
    * Before creating a Plan record, decide whether it's an Academic Plan or a Recruitment Plan you are trying to create or manage.
    * Regardless of the type, start by dealing with the Academic Plan.
4. Creating or Managing an Academic Plan:
    * Create a new Academic Plan and link it to the Academic Program using the appropriate field.
    * Leave the 'Recruitment Interest' field blank for now, as this will be filled after creating the corresponding Recruitment Plan.
5. Creating or Managing a Recruitment Plan (If Applicable):
    * After setting up the Academic Plan, create the Recruitment Plan.
    * Link the Recruitment Plan to the newly created Academic Plan using the lookup field.
6. Finalize the Two-Way Binding:
    * Return to the Academic Plan record.
    * Update the 'Recruitment Interest' field to link to the newly created Recruitment Plan.
    * This establishes a two-way binding between the Academic and Recruitment Plans.

## Important Considerations

* **Validation of Existing Records:** Always confirm the existence of related records before proceeding with the creation of a new Plan record.
* **Respecting Order:** The process must be followed in the specified order to ensure data integrity and correct linkages.
* **Two-Way Binding:** The final step of updating the 'Recruitment Interest' field in the Academic Plan is crucial for maintaining the relationship between the Academic and Recruitment Plans.

_Adhering to this process is essential for maintaining the accuracy and integrity of our recruitment and academic data within Salesforce._