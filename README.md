# Guess-the-position-game
My First Mini Game (Python Language)

mylist=['-','+','*']

from random import shuffle

def shuffled_list(mylist):
    
    shuffle(mylist)
    
    return mylist

def guess_no():

    guess = ''
    
    while guess not in ["0","1","2"]:
    
        guess = input("enter your number : 0,1 or 2")
        
    return int(guess)
        

def check_guess(shuffled,guess):

    if shuffled[guess] == '*':
    
        print("you won!")
        
    else:
    
        print("you lost") 

    print(shuffled)

shuffled = shuffled_list(mylist)

guess = guess_no()

check_guess(shuffled,guess)
