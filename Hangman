import random
words = ["hangman", "cricket", "school", "random", "visual", "python"]
x = random.choice(words)
y = ["_"]*len(x)
max = 6
attempt = 0
guessed = []
print("Welcome to Hangman. In this game you have to try guess the word from guessing each letter one by one.")
while attempt < max and '_' in y:
    print("word:"," ".join(y))
    user = input("Enter a letter")
    if len(user) != 1:
        print("Please enter a single letter")
        continue
    if user.isalpha() == False:
        print("You have not entered a letter")
        continue
    if user in guessed:
        print("This letter has already been guessed. Try again with a different letter.")
        continue
    guessed.append(user)
    if user in x:
        print("Good Guess! '{}' is in the word.".format(user))
        for i in range(len(x)):
            if x[i] == user: 
                y[i] = user
    else:
        attempt +=1
        print("Your guess was wrong. You have {} left".format(max-attempt))
if '_' not in y:
    print("Congratulations! You have successfully guessed the whole word!")
else:
    print("You have run out of attempts and was not able to guess the whole word.")
