balance = 0

def deposit(amount):
    global balance
    balance += amount
    print("Amount deposited successfully.")

def withdraw(amount):
    global balance
    if amount <= balance:
        balance -= amount
        print("Amount withdrawn successfully.")
    else:
        print("Insufficient balance.")

def check_balance():
    print("Current balance:", balance)

print(" Welcome to Simple Banking System")

while True:
    print("\n1. Deposit")
    print("2. Withdraw")
    print("3. Check Balance")
    print("4. Exit")
    choice = int(input("Enter your choice: "))
    if choice == 1:
        amt = float(input("Enter amount to deposit: "))
        deposit(amt)
    elif choice == 2:
        amt = float(input("Enter amount to withdraw: "))
        withdraw(amt)
    elif choice == 3:
        check_balance()
    elif choice == 4:
        print("Thank you for using the bank ")
        break
    else:
        print("Invalid choice ")
