**create variables**
PasswordText   String
secureText   secureString

**sequence**
---> add **input dialog**
  **dialog title**: "Secure Input"
  **input label**: "enter password"
  **input type**: Text Box
  **Value entered**:"PasswordText"

--> open properties---> input --> click --> IsPassword checkbox option and  topmost  true

run the program
