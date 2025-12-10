 #randomnumberguessing
simple python game for guessing random number between(1 -100)
import random

def number_guessing_game():
    print("----- Number Guessing Game -----")
    
    secret_number = random.randint(1, 100)
    attempts = 0

    while True:
        try:
            guess = int(input("Enter your guess (1-100): "))
            attempts += 1
        except ValueError:
            print("Invalid input! Please enter a valid number.")
            continue

        if guess < 1 or guess > 100:
            print("Please guess within the range 1 to 100.")
            continue

        if guess < secret_number:
            print("Too low! Try again.")
        elif guess > secret_number:
            print("Too high! Try again.")
        else:
            print(f"🎉 Correct! The number was {secret_number}.")
            print(f"You guessed it in {attempts} attempts.")
            break
number_guessing_game()
