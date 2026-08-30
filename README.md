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

4. Created Custom Fields on Account, Opportunity and Contacts
   
Account:-
Customer Tier - Picklist,
Customer Segment - Picklist,
Region - Picklist
Industry - Picklist
Customer Health - Formula

Opportunity:-
Deal Type - Picklist
Sales Region - 

Formula Text -IF(
ISPICKVAL( Account.Region__c , 'EMEA'), 'EMEA',
IF(ISPICKVAL( Account.Region__c , 'AMER'), 'AMER',
IF(ISPICKVAL( Account.Region__c , 'APAC'), 'APAC',
IF(ISPICKVAL( Account.Region__c , 'LATAM'), 'LATAM', null))) ),

Approval Required - Formula(Checkbox)- IF(AND(Amount >= 100000, Discount__c>=0.05), True, False),

Risk Level - Formula(Text) - IF( ExpectedRevenue <= 20000, 'Low', 'High')

Contact:- 
Decision Maker - Formula(Checkbox) - IF(ISPICKVAL(Departments__c, 'Finance & Accounting'), true, false)
Preferred Contact Method - Picklist


Security Model

Since we created 3 permission sets for our 3 custom object. However, we could have done it in one permission set but doing it with a separate one can be assigned to other team members as well to not give the access which is not required. We created a permission set group and assigned this to Dipti Agarwal (Standard User) Support Team and Rahul Chaurasiya is Support Manager in role.

<img width="1908" height="816" alt="image" src="https://github.com/user-attachments/assets/2b8d5ee2-62a3-4b93-8477-f4b1cd24243b" />

Moreover the Owd for Account, Opportunity, Contact, Case, Sales Request, Customer Onboarding and Data quality is set to private.

<img width="1903" height="759" alt="image" src="https://github.com/user-attachments/assets/6193a0b4-0cdf-4d3b-81bc-1be6c4f4593e" />


<img width="1902" height="816" alt="image" src="https://github.com/user-attachments/assets/b9516d0b-2e44-4d93-ad2b-98f2a9fe274f" />
