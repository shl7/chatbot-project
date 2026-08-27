# our chatbot   

import datetime
import time 


name = input ("welcome , enter your name ")
presentHour = datetime.datetime.now ().hour 


if presentHour < 12:
    print ("good morning " + name) 

elif presentHour < 18:
    print ("good afternoon " + name)    

elif presentHour < 21:
    print ("good evening " + name)  
else:       
    print ("good night " + name)

# memory for the chatbot to store the responses

responses = {

    # Greetings
    "hello": "Hello! How are you?",
    "hi": "Hi! How can I help you?",
    "hey": "Hey! Nice to meet you.",
    "hii": "Hii! How can I help you?",

    # Introduction
    "what is your name": "My name is ChatBot.",
    "who are you": "I am a simple Python chatbot.",
    "your name": "My name is ChatBot.",

    # How are you
    "how are you": "I am fine, thank you!",
    "how are you doing": "I am doing great!",

    # User information
    "my name is shahil": "Nice to meet you, Shahil!",
    "i am shahil": "Nice to meet you, Shahil!",

    # Help
    "help": "Sure! What do you need help with?",
    "what can you do": "I can answer some basic questions and have a simple conversation.",

    # Time / Date
    "what time is it": "You can check the current time using Python.",
    "what is the time": "You can check the current time using Python.",
    "what is today's date": "You can check today's date using Python.",

    # Programming
    "what is python": "Python is a popular programming language.",
    "what is programming": "Programming is the process of giving instructions to a computer.",
    "what is a variable": "A variable is used to store data in a program.",
    "what is a list": "A list is a collection of items in Python.",
    "what is a dictionary": "A dictionary stores data in key-value pairs.",

    # General
    "thank you": "You're welcome!",
    "thanks": "You're welcome!",
    "good morning": "Good morning! Have a great day.",
    "good afternoon": "Good afternoon!",
    "good evening": "Good evening!",
    "good night": "Good night! Sweet dreams.",

    # Conversation
    "what are you doing": "I am chatting with you.",
    "are you real": "No, I am a simple computer program.",
    "do you like python": "Yes! Python is a great programming language.",
    "do you like me": "Of course! I enjoy chatting with you.",

    # Goodbye
    "bye": "Goodbye! Have a nice day.",
    "goodbye": "Goodbye! See you again.",
    "see you": "See you later!",
}

# method to get the response from the chatbot

def get_response(user_input):
    user_input = user_input.lower()
    
    for key in responses:
        if key in user_input:
            return responses[key]

    return "I'm sorry, I don't understand that."   


# take user input and respond until the user types "exit"

while True:
    user_input = input("ask me question: ")

    if user_input.lower() == "exit":
        print("ChatBot: Goodbye! Have a nice day.")
        break

    bot_response = get_response(user_input)


    print("ChatBot: " + bot_response)
        








