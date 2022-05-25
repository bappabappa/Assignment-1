# Assignment-1
## Namasker sir
Apps Script



#   Task Day -1.(24-05-22)
    1. First I read the documentation .
    2. then see some tutorial on youtube
    3. get some resource shortlisted.
    
# Task Day -2 (25-05-22)
 ### ➡️ First 

        --> open my google drive
        --> make a file name example sheet
        --> open the Apps Script
        -->  make a file name Sheet Example.

### ➡️➡️ Second 

```
    function searcher() {
    const searchString = '';
    const sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
    const searchCol = 1;
    getValues();
    const range = sheet.getRange(2,searchCol,sheet.getLastRow());
    const data = range.getValues();
    Logger.log(data);  
   }
```
output 
        ```
        11:22:49 AM	Info	[[1.0], [2.0], [3.0], [4.0], []]
        ```
### ➡️➡️➡️  Third 
    Access all the contest from the sheet.
 output
    ```
    11:30:55 AM	Info	[[ID, User, Name], [1.0, test-1, yes], [2.0, test-2, yes], [3.0, test -3, ], [4.0, test-4, yes]]
    ```

Here is the code : 

```
    function searcher() {
    const searchString = '';
    const sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
    
    const searchCol = 2;

    const data = sheet.getDataRange().getValues();
    
   }
```
