# THE-RANDOM-NUMBERS
import random
number = random.randint(1, 20)

player_name = input("welcome, your good name please? ")
number_of_guesses = 0
print('I\'m glad to meet you! {} \nLet\'s play a game with you, I will think a number between 1 and 20 then you will guess the number, alright? \nDon\'t forget! You have only 5 chances so guess:'.format(player_name))

while number_of_guesses < 5:
    guess = int(input())
    number_of_guesses += 1
    if guess < number:
        print('Your estimate is too low, go up a little!')
    if guess > number:
        print('Your estimate is too high, go down a bit!')
    if guess == number:
        break
if guess == number:
    print( 'Congratulations! you estimated the correct number. {}, you guessed the number in {} tries!'.format(player_name, number_of_guesses))
else:
    print('sorry! better luck next time ,  you couldn\'t guess the number. \nWell, the number was {}.'.format(number))

