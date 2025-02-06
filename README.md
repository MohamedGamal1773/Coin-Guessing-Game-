# Coin-Guessing-Game-
This is a simple command-line game where the user tries to guess the outcome of a virtual coin toss. The coin can be tossed using one of two randomization methods:
Method 1: random.random() (Generates a floating-point number and determines heads or tails based on its value)
Method 2: random.randint(0,1) (Generates either 0 or 1 to represent heads or tails)
If the user's guess matches the randomly generated result, they win. Otherwise, they lose.
Features:
✅ Choose between two methods to toss the coin
✅ Make a guess between "Heads" or "Tails"
✅ Instant feedback on whether you won or lost
import random
print("""
Welcome to the coin Guessing game
Choose a method to toss the coin
1.Using random.random()
2.Using random.randint()
""")
choice = input("Enter your Choice (1) or (2):\n")
if choice == "1" or choice == "2":
    if choice == "1":
        computer_result1 = random.random()
        if computer_result1 >= 0.5:
            computer_result = "Heads"
        else:
            computer_result = "Tails"
    else:
        computer_result2 = random.randint(0,1)
        if computer_result2 == 0:
            computer_result = "Heads"
        else:
            computer_result = "Tails"
    user_input = input ("Enter your Guess (Heads) or (Tails)\n")
    if user_input.lower() == "heads" or user_input.lower()== "tails":
        if user_input.lower() == computer_result.lower():
            print("Congratulations! You WON!")
        else:
            print("Sorry, You lost!")
            print(f"The Computer`s coin toss result was:\n{computer_result}")
    else:
        print("Invalid Choice please select (Heads) or (Tails) ")
else:
    print("Invalid choice Please Enter your Choice (1) or (2) ")
    
Example Run

Welcome to the coin Guessing game Choose a method to toss the coin 1. Using random.random() 2. Using random.randint() Enter your Choice (1) or (2): > 1 Enter your Guess (Heads) or (Tails) > Heads Congratulations! You WON! 

Technologies Used

Python

random module

Contributing

Feel free to fork this repository and improve the game!

License

This project is open-source and free to use.
Let me know if you need any modifications!

