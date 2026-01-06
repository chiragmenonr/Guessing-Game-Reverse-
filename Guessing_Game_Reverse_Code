import random

# Starting statements
print("Think of a number between 1 and 100.")
userInput = str(input("Click enter when you have it: "))
tries = 0
oldHighGuess = 101
oldLowGuess = 0

if userInput == "": # Starts when the user inputs 0
    guess = random.randrange(1, 101)
    print("I guess " + str(guess))
    
    while userInput != "equal":

        # Guesses higher than previous guesses when given input "high"
        if userInput == "high":
            if guess == 1:
                print("I can't go any lower than 1")
            else:
                oldHighGuess = guess
                guess = random.randrange(oldLowGuess + 1, oldHighGuess)
                tries += 1
                print("I guess " + str(guess))
            
        # Guesses lower than previous guesses when given input "low"
        elif userInput == "low":
            if guess == 100:
                print("I can't go any higher than 100")
            else:
                oldLowGuess = guess
                guess = random.randrange(oldLowGuess + 1, oldHighGuess)
                tries += 1
                print("I guess " + str(guess))
            
        # only takes inputs that aren't only an enter to prevent the
        # following message from coming when the initial enter is done
        elif userInput != "": 
            print("That's not a valid input.")

        # Always asks the following succeeding the earlier statements
        userInput = str(input("Is the number I guessed higher, lower, or \
equal to the number you had in mind?(input 'high', 'low', or 'equal') "))

    # if the guess is correct, then the program stops
    if userInput == "equal":
        print("I knew it!")
        print("It only took me "+str(tries)+" tries.")

# if the user doesn't click enter, then gives an error
else:
    print("That's not a valid input.")
    print("Think of a number between 1 and 100.")
    startingEnter = str(input("Click enter when you have it: "))
