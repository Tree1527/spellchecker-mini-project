words(text): This function takes in a string of text and returns a list of words found in that text using a regular expression to match word characters. It also converts all the words to lowercase.

known(words): This function takes in a list of words and returns a set of words that appear in the frequency distribution (word_ct) of words from the large text file (big.txt).

edits1(word): This function takes in a word and returns a set of all possible words that are one edit away from the input word. The function splits the word into all possible combinations of left and right substrings and then applies different types of edit operations (deletion, transposition, replacement, and insertion) to generate new words.

edits2(word): This function takes in a word and returns a set of all possible words that are two edits away from the input word. It does this by applying the edits1 function twice on the input word.

candidates(word): This function takes in a word and generates a list of possible spelling corrections for that word. It first checks if the word exists in the frequency distribution, if not, it checks the set of words obtained from the edits1 and edits2 functions. If no corrections are found, the input word is returned.

P(word): This function takes in a word and returns the probability of the word appearing in the large text file (big.txt) by dividing the count of the word in the frequency distribution by the total number of words in the frequency distribution.

correction(word, type): This function takes in a word and a string that specifies the type of correction to return. If the type is 'mp', it returns the most probable correction by using the max function on the list of candidates with the P function as the key. If the type is 'all', it returns a list of all possible corrections sorted by probability with the P function as the key.

main(txt): This function takes in a string of text and applies the correction function to each word in the text. If the type is 'mp', it prints the most probable correction for each word. If the type is 'all', it prints all possible corrections for each word.

text_spellcheck(): This function retrieves the text from the textbox in the GUI, splits it into words, and calls the main function to receive the suggestions. It then displays the suggestions in a label on the GUI.
