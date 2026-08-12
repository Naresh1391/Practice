I am debugging a user/group management issue in a legacy Java web application.

Scenario:
- There is a User Group Management screen where a user is selected by Person ID.
- The screen contains two lists:
  1. Available Security Groups
  2. Assigned Security Groups
- Security groups can be moved between these lists using Add/Remove buttons and then saved.

Issue:
- When I remove a normal security group (for example, "AP") from Assigned Security Groups and click Save, the group is removed successfully.
- However, when I remove the security group named "ALL" from Assigned Security Groups and click Save, it does not persist.
- After clicking Save, I get a popup/message similar to "User Modified".
- When I reload or revisit the user, the "ALL" security group appears again in Assigned Security Groups.
- This issue happens only for the "ALL" security group. Other groups can be removed successfully.

Please help me investigate possible root causes.

Can you suggest:
1. What backend validations or business rules might automatically reassign the "ALL" security group?
2. Which Java, Spring, JSP, Controller, Service, DAO, or database code areas I should check?
3. Whether "ALL" could be a default/system-mandatory security group that is re-added during save.
4. What database queries I can run to trace how the "ALL" group is stored and reassigned.
5. What logs, breakpoints, or debugging steps I should use to identify where "ALL" is being added back.
6. Example code patterns that would cause this behavior.

Assume this is a legacy enterprise application with JSP, Java backend, database persistence, and role/security group management.
