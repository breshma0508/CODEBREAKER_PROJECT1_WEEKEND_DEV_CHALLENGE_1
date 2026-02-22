# CODEBREAKER_PROJECT1_WEEKEND_DEV_CHALLENGE_1
Project 1 - Code Breaker Challenge problem 1 Welcome to Code Breaker — the classic logic game of deduction and strategy!

# Code Breaker Game 🎯

In this project, we’ll build the game step by step through three exciting submodules. You’ll primarily work in two key files:

- `game_logic.py` — to implement the core game mechanics.
- `main.py` — to run and test your progress.

Get ready to challenge your mind and crack the code!

---

## 🕹️ The Game: Code Breaker

The computer secretly generates a 4-digit code. Your mission, should you choose to accept it, is to guess this code in **10 attempts or fewer**.

---

## 📜 Game Rules

### 🔐 Secret Code
- The code is exactly **4 digits long**.
- Each digit is a numeric character from `'0'` to `'9'`.
- Duplicate digits are allowed (e.g., `"1123"` is valid).

### 🐂🐄 Feedback System

After each guess, you will receive:

- **Bulls** 🐂 — Digits that are correct **and** in the correct position.
- **Cows** 🐄 — Digits that are correct but in the **wrong position**.

---

## 🚀 First Task: Generating the Secret Code

### ✅ Your Task

Implement a Python function called:

```python
generate_secret_code()
