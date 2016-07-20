### Configure Extension
**Right-click on the icon and select 'Options'**
**Be sure and test the connections after each 'save'**

- username - Your Confluence/Jira username
- Password - Your Confluence/Jira password
- Confluence Url - Full Application Base Url - `https://confluence.<company>.com`
- Jira Url - Full Application Base Url - `https://jira.<company>.com`

### Current Workflow (Confluence)
1. Create a table with data
2. Highlight the table data and use the Jira-Create-Issue Macro to create the issues in Jira
3. Run this extension to supplement and format the Jira issues already created
    - Extension will scan and select the first table it finds on the page with a 'Jira-Issue-Template'
    - Subsequent tables are currently ignored.
    - Map your table header names to the Jira issue columns we have available
    - Each table header may only be mapped to one distinct issue column

### Notes
- The extension will only activate if the page you are on is within your Confluence instance - Set via options
- The extension will also retrieve any attachments from the 'Description' column and add those by default.  This is in addition to the optional 'Attachments' column.
- The following columns are currently available:
  - Summary - Jira Issue Summary
  - Description - Jira Issue Description.  Most formatting is retained.
  - Attachments - Any images in this column will be attached to the issue.
  - Assigned - Grabs first user link.  If none exist, it is left alone.
  - Reporter - Same as above.  SAM - do we really want this?  Jira sets this by default to whoever was logged in when the issue was created.
  - Labels - Splits the text and adds each entry as a label.
- To upload attachments, you must have your confluence site whitelisted within your jira site and 'Allow Incoming' for cors requests.
