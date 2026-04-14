---
title: Features
description: Introduction to the features of the U of T Dataverse Curation Tool

---

Features of the U of T Dataverse Curation Tool
===

# Landing page
[PLACEHOLDER_IMAGE_FOR_LANDING_PAGE]

This is the landing page of the tool. You will have the option to:
1. Start a new dataset review by clicking the 'New dataset' box.
2. Resume a previous dataset review by clicking the 'Resume project' box.
3. Delete a previous dataset review by clicking the 'Delete project' box.


# New dataset page
[PLACEHOLDER_IMAGE_FOR_NEW_DATASET_PAGE]

This is the page for starting a new dataset review. Each dataset review is considered a project in the tool. To start a new dataset review, you will need to input information as stated in the form, including the base url of the repository (e.g., https://demo.borealisdata.ca/), API token of your account, the dataset DOI, the project ID, etc. Plus curator information like the name and email of yourself. 

You also have to select the checklist to use for the review, from the dropdown menu.

Once you submit the form, the tool will start the review and redirect you to the checklist page.

# Checklist page
[PLACEHOLDER_IMAGE_FOR_CHECKLIST_PAGE]

This is the checklist page. The checklist is generated based on the dataset information you provided in the previous step. The tool first retrieves the dataset metadata and files information, and run automated checks for some checklist items (those with the 'automated' badge in the 'Information Location' column) based on the retrieved information.

At the top of the page, you will see the project information (under the 'PROJECT INFORMATION' tab) such as project ID, dataset DOI, dataset title, etc. In the 'CHECKLIST INFORMATION' tab, you will find the the checklist metadata such as the checklist title, version, checklist curation, etc.

Next, below the project and checklist information, you will see the status and time spent dashboard. It shows the count of each status against the total number of checklist items, and the total time spent on the checklist.

Then, you will see filter section, where you can filter the checklist items by the status and priority.

Finally, you will see the checklist table. Each row in the table is a checklist item. The columns in the table include:

1. **ID**: the ID of the checklist item.
2. **Action Item**: the description of the checklist item, which is structured below
      1. The leading item description: this is a concise description of the checklist item
      2. The guidance: this is a more detailed description of the checklist item, providing more context and guidance on how to review the item, such as what information to look for, and how to determine the status of the item.
3. **Information Location**: this section is divided into three parts:
      1. Check type: the badge indicating whether this check item is automated, semiautomatic, or manual.
      2. 'Tools check': If it's an automated or semiautomated check, the specific check that the tool performs for this item will be listed here. A box will follow with the check, showing what the check is and the result of the check if you have run it.
      3. 'Curator Check' information, where is a prompt that tells you what information to look.
4. **Priority**: the priority level for the checklist item, mostly for indicating the level of communication needed with the data depositor to resolve the item. The level of priority is described below:
      1. Info: this indicates that the checklist item is for information only. It's more for contextual information, and (usually) does not require action from the curator.
      2. Required: this indicates that the checklist item is required. It means that if the item is with 'follow-up' status at the end of the review, the dataset will not be able to be published. The curator will need to follow up with the data depositor to resolve the item.
      3. Recommended: this indicates that the checklist item is recommended. It means that if the item is with 'follow-up' status at the end of the review, the dataset can still be published, but it's recommended to follow up with the data depositor to resolve the item. This depends on how many items are with 'follow-up' status, to avoid overwhelming the data depositor with too many follow-up items.
5. **Status**: the status of the checklist item, which can be the following:
      1. Pass: the item has passed the review.
      2. Follow-up: the item requires follow-up with the data depositor.
      3. TBD: to be determined, which means that the curator is not sure about the status of the item, and may need to consult with other curators or the data depositor
      4. Not Applicable: this usually applies to items with 'Info' priority, which means that the item is not applicable to the dataset, and can be marked as 'Not Applicable' without follow-up.
6. **Comments**: the comments for the checklist item. You can fill in the comments with any notes or thoughts you have about the item during the review, such as what information you found for the item, and why you determine the status of the item.
7. **Time Spent**: the time spent on the checklist item. You can log the time spent on each item in the checklist. Click the start `▶︎` button to start the timer when you begin working on an item, and click the stop `■` button when you finish. The time will be logged in this column. If you forget to start the timer, you can also manually input the time spent in this column in the format of MM:SS (e.g. 15:30 for 15 minutes and 30 seconds).


# Resume project page

[PLACEHOLDER_IMAGE_FOR_RESUME_PROJECT_PAGE]

# Delete project page
[PLACEHOLDER_IMAGE_FOR_DELETE_PROJECT_PAGE]