# Salesforce-Portfolio
A collection of Salesforce Administration projects, automation, configuration, reporting, security, and troubleshooting scenarios.
Created a Custom Object Customer Onboarding And fields:- 
Account                - Lookup
Opportunity            - Master Detail
Onboarding Status      - Picklist
Completion Date        - Formula (Date) - IF(ISPICKVAL(Opportunity__r.StageName , 'Closed Won'), Today(), null)

Created Another Object : - Sales Request

Request Type           - Picklist
Account                - Lookup
Opportunity            - Lookup
Request Status         - Picklist
Priority               - Picklist
Request Description    - Long Text Area         

Created Another Object :- Data Quality Issue 

Account                - Lookup
Contact                - Lookup
Issue Type             - Picklist
Status                 - Picklist
Resolution Date        - Date
