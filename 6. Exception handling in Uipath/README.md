**Try catch** -->try --->**assign**
                    
                     **to variable** : num 1
                    
                     **set value** : 10
                
                --->**assign** 
                   
                    **to variable**: num 2
                    **set value**: 0
                
                --->**assign** 
                    
                    **to variable**: result
                   **set value** : num 1\num 2

        ---->catch  system.DivideByZeroException 
            **Body**--->message Box : "Error"+exception.Message

        ---->**Finally**---> message box : "execution completed"
