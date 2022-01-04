# Password-Generator
Programme to generate a random password based on the number of items that you want in it

import random
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to the PyPassword Generator!")
nr_letters= int(input("How many letters would you like in your password?\n")) 
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))

Order not randomised:
#e.g. 4 letter, 2 symbol, 2 number = JduE&!91

#e.g. 4 letter, 2 symbol, 2 number = g^2jk8&P
new_letters = random.choice(letters)
for lets in range (1,nr_letters):
  new_letters += random.choice(letters)

new_symbols = random.choice(symbols)
for syms in range (1, nr_symbols):
  new_symbols += random.choice(symbols)

new_numbers = random.choice(numbers)
for nums in range (1, nr_numbers):
  new_symbols += random.choice(numbers)

new_range = new_letters + new_symbols + new_numbers
print(f"your new password is: {new_range}")

#Hard Level - Order of characters randomised:

random_password = []

for lets in range (1,nr_letters +1):
  random_password += random.choice(letters)

for syms in range (1, nr_symbols +1):
  random_password += random.choice(symbols)

for nums in range (1, nr_numbers +1):
  random_password += random.choice(numbers)


random_password_list = random.sample(random_password, len(random_password))

random_password_3 = ""
for i in random_password_list:
  random_password_3 += i 

print(f"your new random password is: {random_password_3}")

  
