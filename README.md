import random

def play_game():
    print("Welcome to Rock, Paper, Scissors!")
    
    # List of options
    choices = ['rock', 'paper', 'scissors']
    
    while True:
        # User input
        user_choice = input("Enter rock, paper, or scissors (or 'exit' to quit): ").lower()
        
        if user_choice == 'exit':
            print("Thanks for playing! Goodbye!")
            break
        
        if user_choice not in choices:
            print("Invalid choice! Please choose 'rock', 'paper', or 'scissors'.")
            continue
        
        # Computer's choice
        computer_choice = random.choice(choices)
        print(f"Computer chooses: {computer_choice}")
        
        # Determine the winner
        if user_choice == computer_choice:
            print("It's a tie!")
        elif (user_choice == 'rock' and computer_choice == 'scissors') or \
             (user_choice == 'paper' and computer_choice == 'rock') or \
             (user_choice == 'scissors' and computer_choice == 'paper'):
            print("You win!")
        else:
            print("You lose!")

# Run the game
play_game()
