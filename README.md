# reverse-string-by-words
def reverse_string_by_words(input_string):
    words = []
    word = ''
    reversed_string = ''

    # Iterate through the string character by character
    for char in input_string:
        # If the character is not a space, add it to the word
        if char != ' ':
            word += char
        else:
            # If a space is encountered, add the word to the list of words
            words.append(word)
            word = ''
    
    # Add the last word to the list of words
    words.append(word)
    
    # Construct the reversed string by joining words in reverse order
    for i in range(len(words) - 1, -1, -1):
        reversed_string += words[i]
        if i != 0:
            reversed_string += ' '

    return reversed_string

# Example string
input_string = "I want to reverse this string based on words"

# Reverse the string based on words
reversed_words_string = reverse_string_by_words(input_string)
print(reversed_words_string)
