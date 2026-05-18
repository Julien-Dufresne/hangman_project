 # J's Hangman program with explanations

 As part of my studies, we had to use the python languagae to create a small hangman game that consisted of having a hidden word that the user needs to guess the letters until he/she finds the word. 
 He will have a certain amount of attempts to do so.
 
I had to do the following actions: 

User interaction: 
- prompting the user for a letter


Backend :
- defining the hidden word ('test' here)
- defining the amount of attempts (5 here)
- Linking together the number of letters and the lenght of the hidden word
- Creating an empty string called under_word
- Creating an other empty string called new_under_word

- Creating a for loop : adding the amount of letters from the hiden_word as '_' in the new_under_word so the user can see how many letters does the hidden word has
-  





for letter in hidden_word:
  if letter == magic_letter:
    new_under_word = new_under_word + magic_letter
  else:
    new_under_word = new_under_word + "_"

print(new_under_word)



        # will transform the hidden_word letters into _
for letter in hidden_word:
  under_word = under_word + '_'

        # creates a list including index and letter from hidden_word
enumeration_list_ph = []
map_of_hidden_word = list(enumerate(hidden_word))

        # creates a list including index and letter from under_word
enumeration_list_ph2 = []
map_of_under_word = list(enumerate(under_word))


        # finds the index of letters corresponding to guessed_letter


print(map_of_hidden_word)
print(map_of_under_word)
print(under_word)
print(hidden_word)



#-------------
#To do :
  #need to match the magic_letter within the hidden_word
    #(d)need to give the index in the word for the found_letters in the hidden_word
      #with enumerate()
    #need to replace this letter in the under_word (using .replace)
#for i in range(len(hidden_word))

print("Welcome to J's Hangman game. \n You will be asked to give letters to guess the hidden word and you will have 5 attempts to do so")
hidden_word = "test"
under_word = "_" * len(hidden_word)



while under_word != hidden_word: #loop until the word is found
  magic_letter = input("letter:").lower().strip() #prompting to add the letter and removing all Caps and other characters (found online)
  masked_word = "" #startint with an empty word

  for i in range(len(hidden_word)): #taking the number of characters in the hidden word and creating a range of it (0:). For Loop
    if hidden_word[i] == magic_letter: #if the first character of the hidden word is the same as the magic letter,
      masked_word += magic_letter #adding this letter to the magic word
    elif under_word[i] != "_": #also if the first character of the under_word is different of _, meaning we already have found the letter,
      masked_word += under_word[i]   #transfor the _ from the under_word to this character
    else:
      masked_word += "_" # if the character has not being discovered, still keep a _ in the masked_word at this position


  under_word = masked_word  #masked_word become the new under_word with the found letters
  print(masked_word)
print("Well done! You have found the masked word: " , masked_word)
