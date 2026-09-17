program 11

1)create variable 
 name		datatype
dtCustomer	Datatable
customerRow	DataRow
status		String
customerid 	String
customerName	String
email		String
orderid		String
amount          double


create a excel file with fields 
CustomerID	CustomerName	Email	OrderID	Amount	Status
C001	Ravi	ravi@gmail.com	ORD1001	2500	Delivered
C002	Priya	priya@gmail.com	ORD1002	1800	Pending
C003	Arun	arun@gmail.com	ORD1003	3200	Shipped
C004	Divya	divya@gmail.com	ORD1004	1500	Delivered
C005	Kumar	kumar@gmail.com	ORD1005	2750	Pending


2) Drag the Use Excel file activity
     choose file path

3)  in do ,
     drag Read Range activity
       Range  -  Excel.Sheet("Sheet1")
       save to - dtCustomer
property la
   	output - dtCustomer

4)  drag ,Input Dialog activity
     Dialog title  -  "Customer support"
     Input label   -  "Enter customer id"
     Input Type    -   Text Box
     Value entered -   customerid
property la 
	result - customerid

5)   drag assign 
        save to - customerRow
        Value to save - dtCustomer.AsEnumerable().FirstOrDefault(Function(row) row("Customerid").ToString.Trim.Equals(If(customerid, "").Trim))

6)   drag if activity
        condition  -  customerRow IsNot Nothing
    inside then 
        add assign activity
             customerName - customerRow("customerName").ToString
       add assign activity
             email - customerRow("email").ToString
       add assign activity
             orderid - customerRow("OrderID").ToString
       add assign activity
             amount - Convert.ToDouble(customerRow("Amount"))
       add assign activity
             status - customerRow("Status").ToString
       add messagebox activity
              "Customer Name: " + customerName + Environment.NewLine +
"Email: "+ email + Environment.NewLine +
"Order ID: " + orderID + Environment.NewLine +
"Total Amount: ₹" + amount.ToString("0.00") + Environment.NewLine +
"Order Status: " + status

7)inside else part 
	messagebox activity
	"Customer not found. Please check the Customer ID."      

Run the process
