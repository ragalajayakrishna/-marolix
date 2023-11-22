class BankAccount:
    def __init__(self, initial_balance):
        self.balance = initial_balance

    def withdraw(self, amount):
        if amount == 500:
            self.withdraw_500()
        elif amount == 2000:
            self.withdraw_2000()
        else:
            print("Insufficient funds. Withdrawal failed.")

    def withdraw_500(self):
        if self.balance >= 500:
            self.balance -= 500
            print("Withdrawal of 500 successful. Remaining balance:", self.balance)
        else:
            print("Insufficient funds. Withdrawal failed.")

    def withdraw_2000(self):
        if self.balance >= 2000:
            self.balance -= 2000
            print("Withdrawal of 2000 successful. Remaining balance:", self.balance)
        else:
            print("Insufficient funds. Withdrawal failed.")

#Example usage
initial_balance = 5000
account = BankAccount(initial_balance)

#Testing withdrawals
account.withdraw(500)
account.withdraw(2000)
account.withdraw(1000)
account.withdraw(3000)


