class BankAccount
        BankAccount : +String owner
        BankAccount : +Bigdecimal balance
        BankAccount : +deposit(amount)
        BankAccount : +withdrawal(amount)
# AlmexVault




class Square~Shape~{
            int id
            List~int~ position
            setPoints(List~int~ points)
            getPoints() List~int~
        }
        
        Square : -List~string~ messages
        Square : +setMessages(List~string~ messages)
        Square : +getMessages() List~string~
