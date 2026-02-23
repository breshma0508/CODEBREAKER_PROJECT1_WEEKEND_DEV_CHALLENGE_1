# 🧠 Code Breaker – Bulls & Cows Game

A simple Python terminal game where the computer randomly generates a secret 4‑digit code, and you have to guess it in 10 tries or fewer!

This project teaches how to:
- Use random number generation
- Validate user input
- Implement game logic (Bulls & Cows)
- Structure a Python project

---

## 🕹️ Game Rules

- The computer creates a 4‑digit secret code (e.g., `['1','2','3','4']`)
- You guess a 4‑digit number
- After each guess you receive:
  - **Bulls**: correct digit in correct position
  - **Cows**: correct digit in wrong position
- You have **10 attempts** to guess the code correctly

---

## 📁 Project Structure


CodeBreaker/
├── game_logic.py
├── main.py
└── README.md


---

## 🧾 Code Files

### 📌 `game_logic.py`

```python
import random

def generate_secret_code():
    """
    Generates a random 4-digit secret code as a list of strings.
    """
    secret_code = []
    for _ in range(4):
        secret_code.append(str(random.randint(0, 9)))
    return secret_code


def calculate_bulls_and_cows(secret_code, guess):
    """
    Calculates number of bulls and cows.
    Bulls: correct digit in correct position.
    Cows: correct digit but wrong position.
    """
    bulls = 0
    cows = 0

    secret_copy = secret_code.copy()
    guess_copy = guess.copy()

    # Count bulls
    for i in range(4):
        if guess_copy[i] == secret_copy[i]:
            bulls += 1
            secret_copy[i] = None
            guess_copy[i] = None

    # Count cows
    for i in range(4):
        if guess_copy[i] is not None and guess_copy[i] in secret_copy:
            cows += 1
            secret_copy[secret_copy.index(guess_copy[i])] = None

    return bulls, cows

 ---

###  📌 main.py
from game_logic import generate_secret_code, calculate_bulls_and_cows

def get_valid_guess():
    """
    Prompts until user enters a valid 4-digit guess (only digits 0–9).
    """
    while True:
        user_input = input("Enter your 4-digit guess: ").strip()

        if len(user_input) != 4:
            print("Invalid! Must be exactly 4 digits.")
            continue

        if not user_input.isdigit():
            print("Invalid! Only numeric digits allowed.")
            continue

        return list(user_input)


def main():
    print("Welcome to Code Breaker!")
    print("Guess the 4-digit secret code within 10 attempts.\n")

    secret_code = generate_secret_code()
    attempts = 0
    max_attempts = 10

    while attempts < max_attempts:
        guess = get_valid_guess()
        attempts += 1

        bulls, cows = calculate_bulls_and_cows(secret_code, guess)

        print(f"Bulls: {bulls}, Cows: {cows}\n")

        if bulls == 4:
            print(f"🎉 You guessed it right! The secret code was {''.join(secret_code)}")
            return

    print("Invalid! You've used all your attempts.")
    print(f"The secret code was {''.join(secret_code)}")

if __name__ == "__main__":
    main()
⚙️ How to Run

Clone the repository

Open terminal/command prompt

Navigate to the project directory

Run:

python main.py
🧠 How It Works
🟡 Secret Code Generation

We generate 4 random digits (including duplicates), e.g., "1123".
The function returns a list like:

['1', '1', '2', '3']

Using Python’s random.randint(0, 9)

🔢 Bulls and Cows Logic

Bulls: Count for same digit in same location

Cows: Count for correct digit but wrong location

Copies of lists are used to avoid double counting

📦 Input Validation

We check:

✔ 4 characters
✔ All numeric digits (0‑9)

If invalid, user is asked again

🏁 Ending Game

Win: 4 bulls (code cracked)

Lose: 10 wrong guesses → show secret code

💡 Notes

Great beginner project

Ideal for learning Python basics

Can be extended with UI or difficulty levels

---
