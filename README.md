import random

# Thiết lập game
print("Welcome to the Guessing Game!")
print("I'm thinking of a number between 1 and 100. Can you guess what it is?")

# Tạo số ngẫu nhiên
secret_number = random.randint(1, 100)
# Vòng lặp chính của trò chơi
num_guesses = 0
while True:
    # Nhận đoán của người chơi
    guess = int(input("Your guess: "))
    num_guesses += 1

    # Kiểm tra đoán của người chơi
    if guess < secret_number:
        print("Too low! Try again.")
    elif guess > secret_number:
        print("Too high! Try again.")
    else:
        print(f"Congratulations, you guessed the number in {num_guesses} tries!")
        break
