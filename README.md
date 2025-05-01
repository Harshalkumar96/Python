# Python
My Python Work

Password Genrator code in Python 

# Python Password Generator

import random

letters = list('abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ')
numbers = list('0123456789')
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to Password Generator")

n_letters = int(input("How many letters would you like in your password?\n"))
n_symbols = int(input("How many symbols would you like?\n"))
n_numbers = int(input("How many numbers would you like?\n"))

# Generate random characters
password_chars = (
    [random.choice(letters) for _ in range(n_letters)] +
    [random.choice(symbols) for _ in range(n_symbols)] +
    [random.choice(numbers) for _ in range(n_numbers)]
)

print(password_chars)

# Shuffle the combined list
random.shuffle(password_chars)

# Join into a final string
password_final = ''.join(password_chars)

print('Your final password is =>', password_final)
