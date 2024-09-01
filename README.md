# Python-Gaming-Code-
code : 

import random

def guess_number():
    number_to_guess = random.randint(1, 10)
    attempts = 0
    print("Welcome to the Number Guessing Game!")
    print("Guess a number between 1 and 10.")
    
    while True:
        try:
            user_guess = int(input("Enter your guess: "))
            attempts += 1
            
            if user_guess < number_to_guess:
                print("Too low! Try again.")
            elif user_guess > number_to_guess:
                print("Too high! Try again.")
            else:
                print(f"Congratulations! You've guessed the correct number in {attempts} attempts.")
                break
        except ValueError:
            print("Please enter a valid number.")

guess_number()
