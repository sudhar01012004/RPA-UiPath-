Create a variable extractedData > DataType - System.Data.Datatable

in Microsoft edge search something like about subject

in UiPath studio Drag Use application browser activity > click indicate screen > indicate page fully > confirm

inside do activity > drag extract table data activity > click indicate screen > indicate some text > confirm > save & close
in extract table data properties > input/output > extractedData - (variable name)
 
create empty excel file name as > application6.xlsx > save

in UiPath studio Drag Use excel file activity > copy paste the created excel file path (workbook)
inside use excel file there is do > inside do, drag write data table to excel activity 
what to write - extractedData
destination - Excel.Sheet("Sheet1").Range("A1")
