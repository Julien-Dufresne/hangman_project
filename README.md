 # J's Hangman program with explanations

 As part of my studies, we had to use the python languagae to create a small hangman game that consisted of having a hidden word that the user needs to guess the letters until he/she finds the word. 
 He will have a certain amount of attempts to do so.
 
I had to do the following actions: 

User interaction: 
- Prompting the user for a letter


Backend :
- Defining the hidden_word ('test' here)
- Defining the amount of attempts (5 here)
- Linking together the number of letters and the lenght of the hidden word
- Creating an empty string called under_word
- Creating an empty string called masked_word


- Creating a while loop : Until the hidden_word is the same as the under_word, the following applies:
   - Creating a for loop: for a range equal to the lenght of the hidden_word:
      - if a letter in the hidden word is equal to the magic_letter:
         - the corresponding masked_word's letter is replaced by the magic_letter
      - else if the letter in the under_word is different from _, meaning that we have already found this letter,
         - we transform the _ from the under_word by this letter
      - else :
         - if the character has not been discovered yet, we keep a _ in the masked_word at ths position. 
  - under_word becomes masked_word with the found letters



