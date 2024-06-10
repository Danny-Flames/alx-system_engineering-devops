<img src=./image.png width=50%>

### Issue Summary
## Duration of Outage:
The issue persisted for three weeks, from May 1, 2024, 09:00 AM to May 22, 2024, 04:00 PM.

### Impact:
The core banking application’s 'loan product factory' and 'loan management' sections were affected. Specifically, when an admin attempted to create a new collateral asset, the newly created asset did not update in the displayed list without a manual page refresh. This issue affected 100% of the admins using the loan creation feature, causing significant inconvenience and disrupting workflow.

### Root Cause:
A minor spelling error caused by an extra comma in the code prevented the UI from updating the list of collateral assets without a manual refresh.

### Timeline
May 1, 2024, 09:00 AM UTC: Issue detected via customer complaints.
May 1, 2024, 10:00 AM UTC: Initial investigation began by the first assigned developer.
May 3, 2024, 12:00 PM UTC: First developer escalated the issue to a senior engineer after failing to identify the root cause.
May 10, 2024, 09:00 AM UTC: Second developer took over the investigation and began debugging.
May 17, 2024, 11:00 AM UTC: Second developer also failed to fix the issue and escalated it to the team lead.
May 20, 2024, 09:00 AM UTC: Task assigned to me by the team lead.
May 22, 2024, 02:00 PM UTC: Spelling error identified and fixed.
May 22, 2024, 04:00 PM UTC: Issue resolved and changes deployed.
Root Cause and Resolution
Root Cause:
The issue was traced back to a minor spelling error in the code, specifically an extra comma at the end of a spelling. This error caused the condition check to fail, preventing the newly created collateral asset from being added to the cached list of assets, which in turn stopped the UI from updating without a manual page refresh.

### Resolution:
The resolution involved identifying the exact location of the error in the code and removing the extra comma. After this correction, the code functioned as intended, allowing the newly created collateral asset to be added to the cached list and updating the UI accordingly.

### Corrective and Preventative Measures
## Improvements/Fixes:
To prevent such issues in the future, the following measures will be implemented:

Enhanced code review processes to catch minor errors like spelling mistakes.
Implementation of automated tests to validate the correct updating of UI elements after API calls.
Improved logging to quickly identify discrepancies in the data flow.
Tasks to Address the Issue:

Conduct a detailed code review to ensure no similar errors exist.
Add automated tests specifically for the loan product creation workflow.
Update the logging mechanism to provide clearer insights into API call results and UI updates.
Train the development team on the importance of thorough testing and code reviews.
Implement a continuous integration system to automate code quality checks.
By addressing these areas, we aim to improve the robustness of our system and reduce the likelihood of similar issues occurring in the future.