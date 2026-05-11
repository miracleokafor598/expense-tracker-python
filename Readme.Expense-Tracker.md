expenses = []

while True:
    print("\n=== Expense Tracker ===")
    print("1. Add Expense")
    print("2. View Expenses")
    print("3. Total Expenses")
    print("4. Exit")

    choice = input("choose an option: ")
    
    if choice == "1":
        name = input("Enter expense name: ")
        
        try:
           amount = float(input("Enter amount: "))

           expenses.append((name, amount))
           print("Expense added!")

        except:
            print("Please enter a valid number.")

    elif choice == "2":

        if len(expenses) == 0:
            print("No expenses added yet.")

        else: 
            print("\n=== Your Expenses ===")

        for item in expenses:
            print("Name:", item[0], "| Amount:$", item[1])

    elif choice == "3":

        total = 0

        for item in expenses:
            total += item[1]

        print("Total expenses: $", total)

    elif choice == "4":
        print("Goodbye!")
        break
    
    else:
        print("Invalid option.")
