# Introduction
This project involves the implementation of first-order and Nth-order Markov models. The models were used on sentences and writing pieces to calculate transition probabilities and generate new text.
# Pseudocode

```
def build_markov_model(markov_model, new_text, order):
  define start and stop states
  add start state to the text

  is our order greater than 1? if so:
    create a list of tuples that contains every n combo of words starting from i = 0 up until the last word in the text has at least n order of words that succeed it.
    (use this list of tuples for your order of words - if order = 1 just use the text split by whitespace with a start state added to it)


  for each index and current word/order of words in the text:
    if we are at a start state:
      if the start state is already in our markov model:
        if the next word is already in the inner dictionary mapped to our start state:
          add a count val of 1 to the inner dict val
        if the next word isn't in the inner dictionary:
          initialize it with a val of 1
      if the start state isn't already in our markov model:
          initialize it with the outer start key mapped to an inner dictionary with the key being the next word with a value of 1

    if we are at the end of the text:
      if the word/order of words is in the markov model:
        map the end state to 1 in the inner dictionary of the word/order of words
      if this is the first time encountering the word/order of words:
        add the word/order of words as a key in the outer dict and map the end state to 1 in the inner dictionary
      exit the loop

    if we're not at the start or the end of the text and the word/order of words is already in the markov model:
      if the next word in the text has already been encountered after the current word/order of words add 1 to the frequency val of the inner dict associated with that next word
      if the next word in the text hasn't been encountered initialize it as an inner dict key of the current word/order of words with a val of 1

    if we are not at a start state or end state, and haven't encountered the current word/order of words before:
      initialize the current word dict with a inner dict key of the next word in the text with a val of 1

  return the markov model
      
get_next_word
For every state in the Markov model:
  Add up how many times each possible next word occurs
  Convert counts into probabilities by dividing by the total
Look up the list of possible next words for the current state
Look up the corresponding probabilities for those next words
Randomly select one next word using those probabilities
Return the selected word

Markov model for sonnet
Create empty Markov model
Open sonnets.txt
Start with empty string for one sonnet
For each line in the file:
  Remove extra whitespace from the line
If the line is blank:
  Add the sonnet to the Markov model
  Reset the sonnet text to empty
Else:
  Add the line to the current sonnet text
Generate a random text sequence from the Markov model
```

# Successes
Description of the team's learning points

# Struggles
One struggle we faced was making current_word a tuple in the get_random_text function for n > 1. At first, the function we built was taking current_word as a string and trying to replace the tuple with a string. 
# Personal Reflections
## Group Leader
Sneha: Jersha and Connor were both great group members. We were able to meet three times to work through the code together and problem solve.  I had never worked with Markov models before, so I found the implementation to be a little challenging  It was very helpful to talk through the logic involved in Markov model implementation in order find solutions for bugs in our code.

## Other member
Other members' reflections on the project

# Generative AI Appendix
As per the syllabus
