# Druckdaten Sandra zuweisen
YouTrack script/workflow that auto-assigns YouTrack-tickets to a specific colleague. But only if the PROJECTS is "Graphics Team" AND the STATE changes to "Approved" AND if the SUPPLIER contains one of the whitelisted entries.

## How to install:
- see: https://www.jetbrains.com/help/youtrack/server/create-workflow.html (we used the JavaScript-Editor.)
- assign the workflow to a project, see: https://www.jetbrains.com/help/youtrack/server/attach-workflow-to-projects.html


## What it does:
Since we assigned this workflow only to the **Graphics Team** project, it will only work with GT-tickets.

- the script runs when the field **State** changes to the value "Approved"
- it then checks if the field **Supplier** is set to one of these values: 
  - Pollinger
  - Wir machen Druck
  - Caesar Events USA
- if both conditions are met, the workflow:
  - clears all existing assignees
  - assigns Sandra_Schalk to the issue
