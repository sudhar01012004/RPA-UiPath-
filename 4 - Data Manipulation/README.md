**create variable**

Text    string    sequence    "welcome to Ui Studio"
result   boolean  main

**sequence**

  **assign**
    save to -->Text
    value to save-->"welcome to Ui Studio"

 **assign**
    save to -->result
    value to save-->text.Contains ("Studio")  

  **Message Box**-->result.Tostring

**Output**-->True/False
