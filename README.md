import random
import string

print(" Welcome to the Friendly Password Generator!")


try:
    length = int(input("How long should your password be? Enter a number: "))
    if length <= 0:
        print("Password length must be a positive number!")
    else:
        
        characters = string.ascii_letters + string.digits + string.punctuation

        
        password = ''.join(random.choice(characters) for _ in range(length))

 
        print(f"\n here's your strong password:\n {password}")
except ValueError:
    print("Oops! That doesn't look like a number. Please try again with digits only.")
