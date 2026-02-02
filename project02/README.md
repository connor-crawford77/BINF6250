# Introduction
This project involves the implementation of first-order and Nth-order Markov models. The models were used on sentences and writing pieces to calculate transition probabilities and generate new text.
# Pseudocode
Put pseudocode in this box:

```
get_next_word
For every state in the Markov model:
  Add up how many times each possible next word occurs
  Convert counts into probabilities by dividing by the total
Look up the list of possible next words for the current state
Look up the corresponding probabilities for those next words
Randomly select one next word using those probabilities
Return the selected word
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
