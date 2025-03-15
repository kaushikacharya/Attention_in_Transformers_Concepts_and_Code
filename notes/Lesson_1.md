# The Main Ideas Behind Transformers and Attention

- Three main parts of Transformers
  - Word Embedding
  - Positional Encoding
  - Attention

- Word Embedding
  - Converts words, bits of words, and symbols, collectively called **Tokens**, into numbers
  - Why we need numbers?
    - Because Transformers are a type of Neural Network, and Neural Networks only have numbers for input values
- Positional Encoding
  - Helps keep track of word order
- Attention
  - Transformer establishes relationships among words with Attention
  - Example:
    ![Word Association](../images/1_0.png)
    - Attention enables correct association of the word **it** with the word **Pizza**

- Self-Attention
  - Computes how similar each word is to all of the words in the sentence, including itself.
  - Once the similarities are calculated, they are used to determine how the **Transformer** encodes each word
  - Explanation with above example:
    - If you looked at a lot of sentences about **pizza** and the word **it** was more commonly associated with **pizza** than **oven**, then the similarity score for **pizza** will cause it to have a larger impact on how the word **it** is encoded by the **Transformer**
