# Introduction
This repository contains the deliverables for Northeastern University BINF6250 Project 1. The python file contains a script which takes a VCF file and counts the number of occurences of diseases for entries representing rare alleles according to the frequencies from the EXAC database. 
# Pseudocode
Put pseudocode in this box:

```
Read the file
Initialize an empty dictionary where the keys are strings and the values are integers.
Open the file with UTF-8 encoding.
For each line:
  If the line is empty or begins with '#', return a blank list.
  Split the line by '\t' and remove trailing whitespaces and store elements as a list called fields.
  If fields has less than 8 elements, return a blank list.
  Extract the 8th element in fields.
  Store the elements in fields as a dictionary where the keys are strings and the values are either string or none.
    If the element contains '=', then the key is the string before '=' and the value is the string after '='
    If the element does not contain '=', then the key is the element and the value is none.
  From the dictionary, pull the value for the key AF_EXAC. If this value is a placeholder or none, return an empty list.
  If the value cannot be converted to a float, return an empty list. Otherwise, convert value to float.
  If the value is above 0.0001, then return an empty list.
  Pull the value for the key CLNDN from the dictionary.
  If this value is a placeholder or none, return an empty list.
  Split this value by the '|' and store as a list.
  For each element of the CLNDN list, if it is either not_specified or not_provided, do not count it.
  Otherwise, append it to a list of diseases (strings).
  Return the disease list.

For each disease list, elements that appear are either entered into the dictionary as a key with an initial value of 1 if it is the first time it appears or gets 1 added to its tally for each new occurence.


If this fails, exit and raise error

```

# Successes
We learned how to use GitHub to collaborate with others. We learned how to create pull requests and fork repositories. We became familiar with VCF format and how to parse a file line by line. We also learned how to use the pprint Python module to display a dictionary.

# Struggles
In the beginning, we struggled with using GitHub and had to learn how to fork a repository and ensure that the correct branch was being used. 

# Personal Reflections
## Group Leader
Sneha Kini- Ngoc Linh Nguyen and Thu Thu Han were both great partners. When briefly meeting after class, we all shared our strengths and weaknesses in terms of Python coding and GitHub. We were all a bit unfamiliar with GitHub, but we were quickly able to figure out together how to collaborate using pull requests and merges. Everyone was willing to meet outside of class time to get the project done efficiently, and the work load was shared evenly. When coding the actual project, I was a little slow at first since I had never worked with VCF files before, so figuring out how to parse the file with its unique format was a little tricky at first. We did not face any significant challenges and all steps of the project went relatively smoothly. As the team leader, I tried to set up meeting times to make sure the assignment got done in a timely manner.

## Other member
Other members' reflections on the project

# Generative AI Appendix
We asked the Perplexity-based Course Assistant to clarify assignment instructions.
