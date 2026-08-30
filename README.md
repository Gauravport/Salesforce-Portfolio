# Salesforce-Portfolio
A collection of Salesforce Administration projects, automation, configuration, reporting, security, and troubleshooting scenarios. In this project we have designed this org for an IT company which is selling there products to other companies.

1. Created a Custom Object Customer Onboarding And fields:- Account - Lookup,
Opportunity            - Master Detail,
Onboarding Status      - Picklist,
Completion Date        - Formula (Date) - IF(ISPICKVAL(Opportunity__r.StageName , 'Closed Won'), Today(), null)

<img width="1918" height="774" alt="image" src="https://github.com/user-attachments/assets/2fa9a3a9-c8dd-4913-ad75-0b2f702f5b7c" />

Created One Screen flow for Customer Onboarding to create record.

<img width="1918" height="819" alt="image" src="https://github.com/user-attachments/assets/f80562f8-d957-474d-aa6d-d91929b4aa70" />

It is being used on opportunity object in quick action.
<img width="1913" height="809" alt="image" src="https://github.com/user-attachments/assets/d87185c3-0c4a-408c-bf9e-3daf8d8d7cdc" />



2. Created Another Object : - Sales Request, Fields Created: 

Request Type           - Picklist,
Account                - Lookup,
Opportunity            - Lookup,
Request Status         - Picklist,
Priority               - Picklist,
Request Description    - Long Text Area

<img width="1914" height="768" alt="image" src="https://github.com/user-attachments/assets/385be1bf-e0fd-4da2-ad27-0f604495c0d3" />

