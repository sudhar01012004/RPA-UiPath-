
**note**:In this we have 3 questions but we put program for only 2 questions)

data transfer from one system to another
Create a excel file named as "SourceData"
copy and paste the below values

Name	Age	Department
Arun	20	CSE
Ravi	21	IT
Priya	20	ECE

Create another empty excel and saves as "DestinationData"

Open uipath>process
**create a variable**---->dtSource-->datatype--datatable

**drag use excel file**

**workbookpath**>browse the excel file(SourceData)

**Do**>Read Range--Range(Excel.Sheet("Sheet1").Range("A1:C4"))

Properties--Output>Save to>dtSource

outside do

**drag Use excel file**>browse>empty excel(destinationdata)

**Do**>write datatable to Excel
           
           **What to write**----dtSource
           
           **Destination**------Excel.Sheet("Sheet1").Range("A1")
 
 Password Generator

create another process in uipath

**create a variable named**---password-datatype-string

**drag assign**
 
  **to variable**:password
  
  **set value**:Guid.NewGuid().ToString("N").Substring(0,10)

drag message box:
 
 text: "Generated Password :" + password
