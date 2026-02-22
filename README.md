# 🧠 Python Projects for Beginners

## 📌 Project 1 — Code Breaker Challenge (Problem 1)

Welcome to **Code Breaker** — a classic game of logic, deduction, and strategy!

In this project, you'll build the game step by step across three exciting submodules. You will mainly work with:

- `game_logic.py` → where you’ll implement the core game mechanics  
- `main.py` → where you’ll run and test your implementation  

Get ready to challenge your thinking and crack the secret code!

---

## 🎮 About the Game

The computer secretly generates a **4-digit code**.

Your mission?  
Guess the correct code in **10 attempts or fewer**.

---

## 📜 Game Rules

### 🔐 Secret Code Rules

- The code is exactly **4 digits long**
- Each digit is a number from `'0'` to `'9'`
- Duplicate digits **are allowed** (example: `"1123"` is valid)

---

### 🐂🐄 Feedback System

After each guess, the game provides feedback:

- **Bulls 🐂** → Correct digit in the correct position  
- **Cows 🐄** → Correct digit but in the wrong position  

This feedback helps you logically deduce the secret code.

---

## 🚀 First Submodule: Generate the Secret Code

We begin by creating the function that generates the hidden 4-digit code.

---

## ✅ Your Task

Create a function called:

```python
generate_secret_code()

inside the game_logic.py file.

## 🔧 Requirements:

The function must take no arguments

It must randomly generate a 4-digit code

It must return the code as a list of strings

Each element in the list should be a single digit string

Duplicate digits are allowed

The function should NOT print anything

main.py will handle displaying the output.

## ▶️ How to Test Your Code

After implementing the function:

Click Run

Or use the terminal:

python main.py

To run it again:

Click Stop

Then click Run again

## 🧪 Example Outputs

If the generated code is 2234, the console should display:

The random 4-digit number is: ['2', '2', '3', '4']

If the generated code is 7777, the output should be:

The random 4-digit number is: ['7', '7', '7', '7']
