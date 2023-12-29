# Applicant Automations

## Direct students

`Lead - Direct Applicant NEC`

| Filter |
|--------|
| Latest_Opportunity_StageName__c = "Applied" |

***

`Lead - Direct Qualified Applicant NEC`

| Filter |
|--------|
| Latest_Opportunity_StageName__c = "AppEvalDocs" |
| Latest_Opportunity_StageName__c = "AppInterview" |

***

`Applicant - Direct Applicant NEC`

| Filter |
|--------|
| Latest_Opportunity_StageName__c = "AppWUAS" |
| Latest_Opportunity_Parent_Stage__c = "Provisionally Accepted" |
| Latest_Opportunity_Parent_Stage__c = "Finally Accepted" |
| Latest_Opportunity_Parent_Stage__c = "Visa" |
| Latest_Opportunity_Parent_Stage__c = "Arrival" |
| Latest_Opportunity_Parent_Stage__c = "Complete" |

***

`Lead - Direct WOT NEC`

| Filter |
|--------|
| Cancellation_Reason__c = "Waste of time"|

***

## Indirect students

Lead - Indirect Applicant NEC

| Filter |
|--------|
| Latest_Opportunity_StageName__c = "Applied" |