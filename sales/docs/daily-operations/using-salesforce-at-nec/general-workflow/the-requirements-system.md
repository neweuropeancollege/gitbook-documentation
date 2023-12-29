# The Requirement System

## Introduction

The Requirement System is a pivotal component in Salesforce, designed to manage the progression of opportunities through various stages. It is intricately linked to the Opportunity object and interacts with multiple related objects, such as Contacts, Accounts, and potentially Agents or Partners, as well as Application Documents.

## Overview of Opportunity Progression

1. **Initial Stages**:
    * Opportunities begin as _Inquirers_.
    * At this stage, they are classified under the _Inquired_ stage.
    * Opportunities can be moved to the _Confirmed Interest_ stage for distinction.

2. **Transition to Applicant**:
    * The transition from an Inquirer to an Applicant requires the submission of any document.
    * Upon document submission, the opportunity’s record type changes to _Applicant_, altering the layout and content.
    * This triggers the Requirement System Engine.

3. **Requirement System Engine**:
    * It utilizes data from various related records: Opportunity, Contact, Account, and if applicable, other records.
    * It generates a set of tailored Requirement Records for the specific opportunity. For example
        * an opportunity related to a Contact from an EU country will not require visa related application documents.
        * an IELTS verification requirement will be created for opportunities that have a related IELTS application document.

## Categories of Requirement Records

1. **Required Application Documents**: Approved by corresponding Application Document records.
2. **Required Payments**: Approved by corresponding Payment records.
3. **Required Fields**: Approved by the fields in the corresponding records. These can be Opportunity, Contact, Account records.
4. **Required Interviews**: Approved by corresponding Interview records.
5. **Required External Correspondences**: Approved by corresponding External Correspondence records.

Each category forms its own Requirement Records, which need approval by a corresponding object.

## Approval Mechanism

1. **Requirement Specification**: Each Requirement Record specifies the type and nature of the record needed for its approval.
2. **Example**: A Requirement Record for a passport will specify the need for an Application Document of type _Identification_ and subtype _Passport_.

## Progression and Approval

1. **Approval Before Progression**: Each requirement has a field named _To Be Approved Before_, dictating the stage before which it must be approved.
2. **Automatic Progression**: If a requirement is not approved, the opportunity cannot advance beyond the stage defined in the _To Be Approved Before_ field.
3. **Visual Tracking**: Users utilize the Opportunity Chart for a visual overview of an opportunity’s requirements and progression status.

## Flexibility and Restrictions

1. **Adjusting Requirements**: Recruiters can change the _To Be Approved Before_ stage for certain requirements, facilitating the progression of opportunities under special circumstances.
2. **Locked Requirements**: Some requirements are immovable. Attempts to alter these trigger notifications of restriction.
3. **Elevated Privileges**: Users with higher privileges can adjust even the locked requirements, if necessary.

## Conclusion

The Requirement System in Salesforce is a dynamic and robust tool, streamlining the process of managing opportunities. It significantly aids recruiters in efficiently moving opportunities through various stages, ensuring all necessary requirements are met while providing flexibility where needed.
