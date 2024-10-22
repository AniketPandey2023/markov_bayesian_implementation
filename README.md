# Markov Chain and Bayesian Network in Python
This repository provides implementations of two popular probabilistic models:

# a)Markov Chain for generating random text based on input data.
# b)Bayesian Network for simulating medical diagnosis (flu, cough, fever).
## 1. Markov Chain Implementation
### Overview
A Markov Chain is a mathematical model that describes a sequence of possible events, where the probability of each event depends only on the previous one (the "current state"). In this implementation, the Markov Chain is used to generate random sequences of text.

## How It Works
### Initialization:

The model takes an input text and splits it into individual words. These words form the basis of the chain, where each word is linked to the word(s) that follow it.
### Building the Markov Dictionary:

The core of the Markov Chain is a dictionary (or hash map) that maps each word in the text to a list of words that could follow it.
For each word in the input, the model looks at the word immediately after it and stores this "next word" as a possible transition.
For example, if the input text is "the cat sleeps, the cat runs", the word "the" would map to both "cat" and "sleeps", indicating that either word could follow "the".
### Generating Text:

To generate a new sequence, the model starts with a seed word, either chosen randomly or specified by the user.
From this seed word, it picks the next word based on the words associated with it in the dictionary.
This process repeats for a specified number of words, effectively generating a chain of words that mimics the input text's structure.
### Debugging:

The implementation provides a method to display the internal dictionary, making it easy to see how words are linked.
Use Cases
### Markov Chains are often used for text generation tasks such as:

Predictive typing or autocompletion.
Simulating random sequences in creative writing or games.
Modeling random processes in various domains.
## 2. Bayesian Network Implementation
### Overview
A Bayesian Network is a probabilistic graphical model that represents a set of variables and their conditional dependencies. In this implementation, the network simulates a simple medical diagnosis system that predicts whether a person has the flu, cough, or fever, based on predefined probabilities.

### How It Works
### Defining Conditional Probabilities:

The Bayesian Network consists of several nodes (representing variables like flu, cough, and fever), each associated with a conditional probability table (CPT).
For example, the probability of having the flu is predefined (e.g., 10%), and the probabilities of having a cough or fever are dependent on whether the patient has the flu.
### Sampling from the Network:

The model simulates whether the patient has the flu by sampling based on the flu's probability (e.g., a 10% chance of having the flu).
Given whether the patient has the flu, it samples whether they have a cough or fever using the corresponding CPTs.
For instance, if the patient has the flu, there might be an 80% chance of them having a cough and a 70% chance of them having a fever.
Generating a Diagnosis:

The network generates a diagnosis by simulating random samples based on the conditional probabilities. It outputs a combination of flu, cough, and fever statuses for each simulation.
This allows the model to produce various hypothetical outcomes, such as a patient having a cough but not the flu, or having both a fever and the flu.
### Displaying the Conditional Probabilities:

For clarity and understanding, the implementation provides a way to display the conditional probability tables, showing the likelihood of each event.
### Use Cases
Bayesian Networks are widely used in fields such as:

#### Medical diagnosis (like in this implementation).
#### Risk analysis and decision-making.
#### Machine learning for tasks involving probability and uncertainty.
### How to Run the Implementations
To run the code, follow these steps:

Clone this repository to your local machine.
Ensure that Python is installed.
Run the Markov Chain or Bayesian Network scripts to see the models in action.
