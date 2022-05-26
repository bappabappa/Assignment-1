# My concept to implement the assignment
     1. At first take the value of whole sheet.
     2. next the cell having "No" is the target cell
     3. Remove them all having "no " string.
     4 create a new array and push the other all value containing "YES".
     5 Next new array value will be copied by (setValues() method to new sheet.)




# 1 Search String Code 
```

    function searcher() {
    const searchString = 'kaka';
    const sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
    // const searchCol = 1;
    const searchCol = 2;

    const data = sheet.getDataRange().getValues();
    // const range = sheet.getRange(2,searchCol,sheet.getLastRow());
    // const data = range.getValues();
    Logger.log(data);
    const result = data.finder(searchString);
    Logger.log( searchString + " is presnet in ID: "+ result);
    // const arr  =[];
    // arr.push(result);
    // Logger.log(arr);
}

Array.prototype.finder= function(val){
  if(val=="") return false;

  for(let i=0; i<this.length;i++){
    if (this[i].toString().indexOf(val)>-1)return i;
  }
  return -1;
}

### output:

```
    12:49:07 PM	Info	[[ID, User, Name], [1.0, test-1, yes], [2.0, test-2, yes], [3.0, test -3, no], [4.0, test-4, yes], [5.0, dada, yes], [6.0, mama, yes], [7.0, kaka, no ]]
12:49:07 PM	Info	kaka is presnet in ID: 7
    ```
# 2 Copy Method from one sheet to another:
```function copyRowsValues() {
  let spreadSheet = SpreadsheetApp.getActiveSpreadsheet();
  let sourceSheet = spreadSheet.getSheetByName("Source");

  let sourceRange = sourceSheet.getDataRange();
  let sourceValues =sourceRange.getValues();

  let rowCount = sourceValues.length;
  let columnCount = sourceValues[0].length;

  //Now working with the target value
  let targetSheet = spreadSheet.getSheetByName("Target");
  let targetRange = targetSheet.getRange(1,1,rowCount,columnCount);

//copy the sourceValue to Target destination.
  targetRange.setValues(sourceValues);
  Logger.log("values are copied :)")


}





