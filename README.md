# ECE2112 Programming Problems

This repository holds Python scripts designed to tackle different programming challenges in ECE2112. Below is a summary of each script provided.


### 1. Alphabet Soup Problem
``` python
def alphabetize_word(word):
    #Check if the input is a single word (no spaces allowed)
    if " " in word:
        #Return error message if there are space/s
        return "Error: Please enter a single word without spaces."
    
    #Sort the letters in alphabetical order 
    #"(sorted(word)) organizes the letters from A to Z
    #"''.join" put together the sorted word into a single string
    sorted_word = ''.join(sorted(word))
    #Return the newly sorted word
    return sorted_word

#Example usage
input_word = input("Please enter a single word: ") # Ask the user to input a single word (spaces are not allowed) 
result = alphabetize_word(input_word) # Call the function with the user's input
result #Print the result
```

### 2. Emoticon Problem
``` python
def emotify(sentence):
    # Create dictionary the match word/s with the emojis
    emoticons = {
        "smile": ":)",
        "grin": ":D",
        "sad": ":((",
        "mad": ">:("
    }
    
    # Replace the words with corresponding emoticons
    words = sentence.split() # Break sentence into individual words 
    new_sentence = ' '.join([emoticons.get(word, word) for word in words]) # Replace the word/s with their corresponding emoticons. If not applicable then no need to change that word. 

    # Return the new sentence with their corresponding emoticons
    return new_sentence

#Example usage
user_input = input("Enter a sentence: ") # Ask user to input a sentence
result = emotify(user_input) # Call the emotify function to change / replace the words with emoticons if applicable 
print(result) # Print the result
```

### 3. Unpacking List Problem
``` python
# Ask user to input integers that are separated by a space. 
listOfIntegers = list(map(int, input("Enter the numbers separated by spaces: ").split()))

# Split the list into 3 sections. First - first integer. Last - last integer. Middle - everything in between of first and last. 
first, *middle, last = listOfIntegers

# Printing the variables
print("first:", first) # Print the first number
print("middle:", middle) # Print the middle numbers 
print("last:", last) # Print the last number
```


