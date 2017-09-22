# jQuery
SpiderBasic-Module to use jQuery (https://jquery.com/)

# Example:

```
IncludeFile "jQuery.sbi"

UseModule jQuery
  
  Define Table, TableRow, TableCell
  Define rowCounter, cellCounter
  
  Table = Element("<table />") ; Create a table element
  
  SetAttribute(Table, "border", "1") ; set the border attribute
  
  SetCSS(Table, "background-color", "white") ; set the background-color to white
  
  SetCSS(Table, "position", "absolute") ; set the position...
  SetCSS(Table, "top", "100px")
  SetCSS(Table, "left", "100px")
  
  For rowCounter = 0 To 9 ; let's create 10 table rows
    
    TableRow = Element("<tr />") ; create a table row element
    
    For cellCounter = 0 To 9 ; let's create 10 table cells per row
      
      TableCell = Element("<td />") ; create a table cell element
      
      SetText(TableCell, "Row " + rowCounter + " / Cell " + cellCounter) ; write some text into the cell
      
      Append(TableRow, TableCell) ; append the new cell element to the current row element
      
    Next
    
    Append(Table, TableRow) ; append the new row element to the table element
    
  Next
  
  Body = Element("Body") ; get the body element
  
  Append(Body, Table) ; and append the table element to the body element
  
UnuseModule jQuery
```

## Lizenz

[MIT](https://github.com/spiderbytes/jQuery/blob/master/LICENSE)
