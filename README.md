# CODEBREAKER_PROJECT1_WEEKEND_DEV_CHALLENGE_1
Project 1 - Code Breaker Challenge problem 1 Welcome to Code Breaker — the classic logic game of deduction and strategy!

In this project, we’ll build the game step by step through three exciting submodules. You’ll primarily work in two key files: game_logic.py to implement the core mechanics, and main.py to run and test your progress. Get ready to challenge your mind and crack the code!

The Game: Code Breaker

The computer secretly generates a 4-digit code. Your mission, should you choose to accept it, is to guess this code in 10 attempts or fewer.

Game Rules & How It Works:

Secret Code:

The code is exactly 4 digits long.
Each digit is a numeric character from '0' to '9'.
Duplicate digits are allowed (e.g., "1123" is a valid code).
Feedback: After each guess you make, you'll receive feedback:

Bulls: The number of digits in your guess that are correct AND in the correct position.
Cows: The number of digits in your guess that are correct BUT in the wrong position.


Our First Task: Generating the Secret Code

Let's start with the very first submodule: creating the secret code itself.

Your Task
Implement a Python function generate_secret_code() within the game_logic.py file.

This function should take no arguments.
It must randomly generate a 4-digit secret code.
The function should return this code as a list of strings, where each string is a single digit.
Update your code in game_logic.py and then click on 'Run' to test.

Note:

Ensure your generate_secret_code() function returns the secret code. It should not print anything itself. The printing is handled by main.py.
To test your code, click the 'Run' button. If you want to test again, you can either type python main.py in the terminal or click the 'Stop' button and then the 'Run' button again.
Sample Cases
For example, if the randomly generated secret code is 2234, the console output (from main.py which will call your function) should be:

The random 4-digit number is: ['2', '2', '3', '4']
Similarly, if the secret code is 7777, the expected output is:

The random 4-digit number is: ['7', '7', '7', '7']
