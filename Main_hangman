import random

word_list = [
    "animal", "autumn", "bakery", "banana", "bottle", "bounce", "breeze", "bridge", 
    "bucket", "burger", "button", "camera", "candle", "carrot", "castle", "cereal", 
    "cheese", "cherry", "church", "circle", "closet", "clumsy", "coffee", "cookie", 
    "copper", "create", "dancer", "desert", "doctor", "donkey", "dragon", "energy", 
    "falcon", "fierce", "flower", "folder", "forest", "forget", "friend", "galaxy", 
    "garlic", "gentle", "guitar", "hacker", "helmet", "hunter", "island", "jacket", 
    "jaguar", "juggle", "jungle", "laptop", "lizard", "market", "memory", "mirror", 
    "monkey", "muffin", "museum", "nature", "ocean", "orange", "pastry", "pencil", 
    "pepper", "pigeon", "pirate", "planet", "pocket", "police", "potato", "purple", 
    "puzzle", "rabbit", "random", "rocket", "router", "school", "screen", "search", 
    "server", "silent", "silver", "spider", "spring", "sprint", "summer", "switch", 
    "system", "tennis", "ticket", "tomato", "travel", "turtle", "wallet", "wander", 
    "weasel", "window", "winter", "yellow"
]

word = random.choice(word_list)
guessed = []
wrong_guess = 0
max_attempt = 5

hangman_states = [
    """
     -----
     |   |
         |
         |
         |
    =========
    """,
    """
     -----
     |   |
     O   |
         |
         |
    =========
    """,
    """
     -----
     |   |
     O   |
     |   |
         |
    =========
    """,
    """
     -----
     |   |
     O   |
    /|\  |
         |
    =========
    """,
    """
     -----
     |   |
     O   |
    /|\  |
    /    |
    =========
    """,
    """
     -----
     |   |
     O   |
    /|\  |
    / \  |
    =========
    """
]

print("===================")
print("Welcome to Hangman!")
print("===================")

while wrong_guess < max_attempt:
    display = ""
    for letter in word:
        if letter in guessed:
            display += letter + " "
        else:
            display += "_ "

    print(hangman_states[wrong_guess])
    print(f"Word: {display}")

    if "_" not in display:
        print("Congratulations! You guessed it!")
        print(f"The word was: {word}")
        break

    guess = input("Guess a letter: ").lower()

    if len(guess) != 1 or not guess.isalpha():
        print("Please enter one letter only.")
        continue

    if guess in guessed:
        print("You already guessed the letter.")
        continue

    guessed.append(guess)

    if guess in word:
        print("Correct guess!")
    else:
        wrong_guess += 1
        print("Wrong guess!")

else:
    print(hangman_states[wrong_guess])
    print("Game Over!")
    print(f"The word was: {word}")
