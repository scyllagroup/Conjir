### Configure Conjir
**Click or Right-click on the icon and select 'Options'**

**Enter your Confluence/Jira Information**
- username - Your Confluence/Jira username
- Password - Your Confluence/Jira password
- Confluence Url - Full Application Base Url - `https://confluence.<company>.com`
- Jira Url - Full Application Base Url - `https://jira.<company>.com`

**Be sure and test your new connections**

### Confluence to Jira Workflow
1. First, create your requirements table with formatted data & use the prebuild "Jira Issue Creator" to create your Jira Issues.  With your Jira Issues created your are ready to use Conjir.
2. Launch the Conjir extension by right clicking the icon in the browser bar and hitting *Launch*.
3. Int the "Format Jira Tasks" window, choose which columns within your Confluence table you want to modify issues of within Jira.
    - Extension will scan and select the first table it finds on the page with a 'Jira-Issue-Template'.
    - Subsequent tables are currently ignored.
    - Map your table column header names to the Jira issue columns we have available.
    - Each table header may only be mapped to one distinct issue column.
3. Click *Submit* to run this extension and update the Jira issues already created.

### Notes (REMOVE)
- The extension will also retrieve any attachments from the 'Description' column and add those by default.  This is in addition to the optional 'Attachments' column.
- To upload attachments, you must have your confluence site whitelisted within your jira site and 'Allow Incoming' for cors requests.
