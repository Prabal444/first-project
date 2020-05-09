# 1. The computer will think of 3 digit number that has no repeating digits.
# 2. You will then guess a 3 digit number
# 3. The computer will then give back clues, the possible clues are:
#
#     Close: You've guessed a correct number but in the wrong position
#     Match: You've guessed a correct number in the correct position
#     Nope: You haven't guess any of the numbers correctly
#
# 4. Based on these clues you will guess again until you break the code with a
#    perfect match!
def enter_guess():
    '''
    Asks for the number guess and transforms the string to a list.
    '''
    print("ENTER YOUR 3 DIGITS GUESS")
    return list(input("What is your guess?"))
#generating a function for taking the guess and digits as input
def userGuess(guess,digits):
    if guess == digits:
        return "CODE CRACKED!"
    clues = [] #empty list
    #compare guess to CODE
    for ind,num in enumerate(guess):
        if num == digits[ind]:
            clues.append("Match")
        elif num in digits:
            clues.append("Close")
    if clues == []:
        return ["Nope"]
    else:
        return clues
#run game
import random
digits = list(range(10))#converting the items in list into string
random.shuffle(digits)
x = digits[0:3]
x = [str(num) for num in x]
print(x)

#an empty cluse report to start with
clueReport = []

#keep asking until user has gotten it straight
while clueReport != "CODE CRACKED!":

    #Ask for guess
    guess = enter_guess()
    #TO RESTRAIN TEH USER FROM ENTERING MORE THAN 3 DIGITS
    import re
    if len(guess)>3:
        print("only three digit guess")
        exit()

    #give the clues
    clueReport = userGuess(guess,x)
    print("here is the result of the guess : ")
    print(clueReport)
