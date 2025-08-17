# Guess-the-position-game

**My First Mini Game (Python Language)**

## Description

This is a simple command-line Python game where you try to guess the position of the `*` symbol after the list is shuffled.  
You will be prompted to enter a number (0, 1, or 2) to guess the position. If you guess correctly, you win!

## How to Play

1. Run the Python script (`python game.py`).
2. Enter your guess: 0, 1, or 2.
3. See if you guessed the correct position of the `*`!

## Code

```python
mylist = ['-', '+', '*']

from random import shuffle

def shuffled_list(mylist):
    shuffle(mylist)
    return mylist

def guess_no():
    guess = ''
    while guess not in ["0", "1", "2"]:
        guess = input("Enter your number: 0, 1, or 2 > ")
    return int(guess)

def check_guess(shuffled, guess):
    if shuffled[guess] == '*':
        print("You won!")
    else:
        print("You lost")
    print(shuffled)

shuffled = shuffled_list(mylist)
guess = guess_no()
check_guess(shuffled, guess)
```

## Example Output

```
Enter your number: 0, 1, or 2 > 2
You lost
['*', '-', '+']
```

## Requirements

- Python 3.13.5

## Author

AKRISHT-VERMA
