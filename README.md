import random
import os
#Simple chat program
#Responds randomly with one of four preprogrammed responses
name = input("What's your name?\n")


def generate_response(user_input):
  responses = [
    "How interesting!",
    "You don't say!",
    "Very cool!",
    "Programming is fun!",
    "Ohh really",
    "Sounds good!",
    
  ]
  return random.choice(responses)


def init_chat():
  quit_character = 'q'
  
  user_input = input(f'Hello {name}, how are you?\n')

  while user_input != quit_character:
    #Ask the user for more input, then use that in your response
    user_input = input(generate_response(user_input) + "\n")
    print(f'{name}, type {quit_character} if you wanna stop the chat\n')
    user_input = input(f'{name}, How is the weather there?\n')
    user_input = input(generate_response(user_input) + "\n")
    user_input = input(f"{name}, What's your favorite season")
    user_input = input(generate_response(user_input) + "\n")
    user_input = input(f'{name}, Who is your favorite singer?\n')
    user_input = input(generate_response(user_input) + "\n")
    user_input = input(f"{name}, What's your favorite song?\n")
    user_input = input(generate_response(user_input) + "\n")
  
os.system('clear')

if __name__ == "__main__":
  init_chat()
