# Coin-Guessing-Game
This is a simple command-line game where the user tries to guess the outcome of a virtual coin toss. The coin can be tossed using one of two randomization methods:
Method 1: random.random() (Generates a floating-point number and determines heads or tails based on its value)
Method 2: random.randint(0,1) (Generates either 0 or 1 to represent heads or tails)
If the user's guess matches the randomly generated result, they win. Otherwise, they lose.
# Features:
✅ Choose between two methods to toss the coin
✅ Make a guess between "Heads" or "Tails"
✅ Instant feedback on whether you won or lost
import random

print("""
Welcome to the Coin Guessing Game!  
Choose a method to toss the coin:  
1. Using random.random()  
2. Using random.randint()  
""")

choice = input("Enter your choice (1) or (2):\n")

if choice in ("1", "2"):
    if choice == "1":
        computer_result = "Heads" if random.random() >= 0.5 else "Tails"
    else:
        computer_result = "Heads" if random.randint(0, 1) == 0 else "Tails"

    user_input = input("Enter your guess (Heads or Tails):\n").strip().capitalize()

    if user_input in ("Heads", "Tails"):
        if user_input == computer_result:
            print("🎉 Congratulations! You WON!")
        else:
            print(f"❌ Sorry, you lost! The computer's coin toss result was: {computer_result}")
    else:
        print("⚠ Invalid choice! Please enter 'Heads' or 'Tails'.")
else:
    print("⚠ Invalid choice! Please enter '1' or '2'.")
      
    
# Example Run

Welcome to the coin Guessing game Choose a method to toss the coin 1. Using random.random() 2. Using random.randint() Enter your Choice (1) or (2): > 1 Enter your Guess (Heads) or (Tails) > Heads Congratulations! You WON! 

# Technologies Used

Python

random module

# Contributing

Feel free to fork this repository and improve the game!

# License

This project is open-source and free to use.
Let me know if you need any modifications!

