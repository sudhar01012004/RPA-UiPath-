**create varaibles**

     Name	  Type	   Default
captchaCode	 String	   ""
userInput	  String	   ""
isMatch	    Boolean  	False
attempts   	Int32     	0

**drag assign**-->**set to**-captchaCode,**Value**---->Path.GetRandomFileName().Replace(".","").Substring(0,6).ToUpper()

**add msg box**--->Text-->"Your CAPTCHA code is: " + captchaCode

**add do while**--->*8give this code in condition**-->isMatch = False And attempts < 3

Inside the Do While, add:
**Input Dialog activity**

**Label**: "Enter the CAPTCHA code shown"

**Title**: "CAPTCHA Verification"

Result stored in userInput

Assign activity
 
  **Assign 1**:
    
    **To variable**: isMatch
    
    **Set value**: userInput.Trim().ToUpper() = captchaCode
 
  **Assign 2**:
    
    **To variable**: attempts
    
    **Set value**: attempts + 1

Add If activity outside the do while or loop:
    
    **Condition**: isMatch
    
    **Then: Message Box**→ "CAPTCHA Verified Successfully!"
    
    **Else: Message Box**→ "Incorrect. Attempts left: " + (3 - attempts).ToString()

After the Do While loop, add an If activity:
  
  **Condition:** Not isMatch
  
  **Then: Message Box** → " Verification failed. Too many attempts."
