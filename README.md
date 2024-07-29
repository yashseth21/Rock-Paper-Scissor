# Rock-Paper-Scissor
import random

def get_computer_choice():
    choices = ['rock', 'paper', 'scissors']
    return random.choice(choices)

def determine_winner(player_choice, computer_choice):
    if player_choice == computer_choice:
        return "It's a tie!"
    elif (player_choice == 'rock' and computer_choice == 'scissors') or \
         (player_choice == 'paper' and computer_choice == 'rock') or \
         (player_choice == 'scissors' and computer_choice == 'paper'):
        return "You win!"
    else:
        return "You lose!"

def main():
    print("Welcome to Rock, Paper, Scissors!")

    while True:
        player_choice = input("Enter rock, paper, or scissors (or 'exit' to quit): ").lower()

        if player_choice == 'exit':
            print("Thanks for playing!")
            break

        if player_choice not in ['rock', 'paper', 'scissors']:
            print("Invalid choice. Please choose rock, paper, or scissors.")
            continue

        computer_choice = get_computer_choice()
        print(f"Computer chose: {computer_choice}")

        result = determine_winner(player_choice, computer_choice)
        print(result)
        print()  # Print an empty line for better readability

if __name__ == "__main__":
    main()
