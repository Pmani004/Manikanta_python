import random
class BankDetail:
    
    people={}
    def CreateAccount(self,accountno):
        self.balance=0
        self.name=input("Enter account holder name")
        self.age=int(input("Enter account holder age"))
        self.city=input("Enter city of residence")
        print("account creation successful")
        self.accountno=accountno
        BankDetail.people[self.accountno]=[self.name,self.age,self.city,self.balance]
    def getBalance(self):
        print("Available balance:",BankDetail.people[self.accountno][-1])
    def getDetails(self):
        print("Name of account holder",self.name)
        print("Age of the holder",self.age)
        print("city of the holder",self.city)
    def deposit(self,amount):
        self.balance+=amount
        BankDetail.people[self.accountno][-1]+=amount 
        print(amount,"deposited in account number")
        print(self.balance,"is your balance")
    def withdraw(self,amount):
        if amount>self.balance:
            print("Balance insufficient")
        else:
            BankDetail.people[self.accountno][-1]-=amount 
            self.balance=self.balance-amount
            print("remaining balance",self.balance)
    def Fundtransfer(self):
        accno=int(input("Enter account no"))
        amount=int(input("Enter amount"))
        if amount>self.balance:
            print("Balance insufficient")
        else:
            BankDetail.people[self.accountno][-1]-=amount 
            BankDetail.people[accno][-1]+=amount 
            self.balance=self.balance-amount
            print("remaining balance",self.balance)

        


b=BankDetail()
c=BankDetail()
b.CreateAccount(12345678)
c.CreateAccount(87654321)
b.getDetails()
b.deposit(5000)
b.withdraw(1000)
b.Fundtransfer()
c.getBalance()
