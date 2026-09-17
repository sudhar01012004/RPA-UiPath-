

create variable 

customerEmail         string        Main
total                 Double        Main
quantity              Int32         Main
price                 Double        Main
productName           String        Main
CustomerName          String        Main
InvoiceNumber         String        Main
InvoiceText           String        Main



Input Dialog ---> Dialog Title: "Invoice Details"
                  Input Label: "Enter customer Name"
                  Input Type : Text Box
                  Value entered : customerName

Input Dialog ---> Dialog Title: "Invoice Details"
                  Input Label: "Enter customer Email"
                  Input Type : Text Box
                  Value entered : customerEmail

Input Dialog ---> Dialog Title: "Invoice Details"
                  Input Label: "Enter Invoice Number"
                  Input Box : Text Box
                  Value entered : Invoice Number

                  
Input Dialog ---> Dialog Title: "Product Details"
                  Input Label: "Enter Product Name"
                  Input Type : Text Box
                  Value entered : productName


Input Dialog ---> Dialog Title: "Product Details"
                  Input Label: "Enter Quantity"
                  Input Type : Text Box
                  Value entered : quantity

Input Dialog ---> Dialog Title: "Product Details"
                  Input Label: "Enter Price Per Unit"
                  Input Type : Text Box
                  Value entered : price

assign ----> To variable : total
             set value : quantity*price


assign ----> To Variable : invoiceText 
             set value : "============================================================"
                            + Environment.NewLine +
                           "INVOICE" + Environment.NewLine +
                            Environment.NewLine +
                             "------------------------" + Environment.NewLine +
                             "Invoice Number: " + invoiceNumber + Environment.NewLine +
                             "Customer Name: " + customerName + Environment.NewLine +
                                 "------------------------" + Environment.NewLine +
                             "Product: " + productName + Environment.NewLine +
                                  "Quantity: " + quantity.ToString + Environment.NewLine +
                                     "Price Per Unit: ₹" + price.ToString + Environment.NewLine +
                                        Environment.NewLine +
                                   "------------------------" + Environment.NewLine +
                                     "Grand Total: ₹" + total.ToString + Environment.NewLine +
                                      "============================================================"


create a empty word document  and save it 

word application Scop -----> file path : copy the path of that doc 
                                    Do : append text ----> text: invoiceText
                             save document as pdf ---> file path: "C:\Users\Admin\Desktop\INVOICE_ " + InvoiceNumber.ToString
                             message box --> Text : "Invoice created successfully"
output: enter quantity =2
        enter price pre unit = 100
        enter product name = Butter 
        enter Invoice Number = INV001
        enter customer email = moni2004@gmail.com
        enter Customer Name = Moni
        Invoice created successfully
