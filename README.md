# ATM
This project is a simple ATM Machine simulation in Python that allows users to perform basic banking operations such as PIN authentication, balance inquiry, cash withdrawal, deposit, and language selection. It is a beginner-friendly project that demonstrates the use of loops, conditionals, and user input handling in Python.
'''ATM Machine'''
def ATM():
    balance=int(input("enter balance:"))
    pin="1625"
    withdraw=5000
    print("    WELCOME TO ATM"    )
    print("select language")
    print("English")
    print("Telugu(తెలుగు)")
    print("Hindi(हिन्दी)")
    lang_choice=input("enter your choice:")
    if lang_choice=="1":
        lang="English"
    elif lang_choice=="Telugu(తెలుగు)":
        lang="Telugu(తెలుగు)"
    elif lang_choice=="Hindi()":
        lang="Hindi"
    else:
        print("Invalid choice")
        lang="English"
    print(f'\n you selected:{lang}')
    enter_pin=input("Enter your pin:")
    if enter_pin!=pin:
        print("Incorrect Pin.Try Again")
        return
    print("\n---->ATM Menu<----")
    print("1.Check Balance")
    print("2.Deposit Money")
    print("3.Withdraw Money")
    print("4.Exit")
    choice=input("Enter Your Choice:")
    if choice=="Check Balance":
        print(f"your current balance is:{balance}")
    elif choice=="Deposit Money":
        amount=float(input("enter amount to deposit:"))
        balance+=amount
        print(f"{amount} deposite successfully")
        print(f"{amount} deposited successfully")
        print(f"updated balance:{balance}")
    elif choice=="Withdraw Money":
        amount=float(int(input(f"enter amount to withdraw amount:")))
        if amount>withdraw:
            print("withdraw amount exceed! max allowed per transaction is {withdraw}")
        elif amount>balance:
            print("Insufficient balance")
        else:
            balance-=amount
            print(f"updated balance:{balance}")
    elif choice=="Exit":
        print("Thank You")
    else:
        print("Invalid Choice")
ATM()

