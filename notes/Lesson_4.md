# Self-Attention vs Masked Self-Attention

- Explains the need for giving similar numbers to similar words used in similar ways.
  - Example:
    - Pizza is **great**.
    - Pizza is **awesome**.
- Explains the requirement for vector representation of words
  - To represent the different contexts the words can be used.
    - Example
      - Pizza is **great**.
      - My cellphone is broken, **great**.
    - Example shows that same word can be used in positive as well as negative way.

## Word Embeddings

- The number of activation functions determines how many numbers we will use to represent each word.
  ![Word Embeddings](../images/4_0.png)

- Weights are the word embedding values
  - Initialized randomly but trained to update these values
  ![Weights: Embedding values](../images/4_1.png)

  - Idea of training is to create similar embedding for **great** and **awesome** as both words appear in similar context in the training data.
  - The below figure shows the initial random value.
  ![Random embedding values](../images/4_2.png)

- Predicting next word
  - We want each word in the training data to predict the next word.
  - Prediction with initialized random values might predict incorrect next word for a word.
    - Here **pizza** predicts next word as **great** instead of **is**
    ![Next word prediction with initialized weights](../images/4_3.png)
  - Post-training next prediction improves
    - Here **pizza** predicts next word as **is**
    ![Next word prediction with trained weights](../images/4_4.png)
  - Post-training **great** and **awesome** cluster together
    ![Post training vector display](../images/4_5.png)

- Adding more context
  - Instead of using only one word use more previous words to predict next word
  - This is required as training gets bigger and sentence length increases.
  ![Adding more context for predicting next word](../images/4_6.png)
  - **1**: Assigned to the word used for context
  - Word ordering is not considered

## Context Aware Embeddings

![Context Aware Embeddings](../images/4_7.png)

- To overcome non-consideration of word order, Transformers use **Positional Encoding**.
- This is followed by an **Attention** layer that helps establish relationships among words.
  - ![Attention layer](../images/attention_ex_1.png)
- **Context aware embeddings** (also called **contextualized embeddings**) can cluster
  - Similar sentences
    ![Clustering similar sentences](../images/4_8.png)
  - Similar documents
    ![Clustering similar documents](../images/4_9.png)

## Encoder-Only Transformer

- Encoder-Only Transformer uses only **Self-Attention**
  ![Encoder-Only Transformer](../images/4_10.png)

## Decoder-Only Transformer

![Decoder-Only Transformer](../images/4_11.png)

- Self-Attention vs Masked Self-Attention
![Self-Attention vs Masked Self-Attention](../images/4_12.png)
  - Self-Attention: Considers both before and after words
  - Masked Self-Attention: Ignores words after the word of interest
- Encoder-only Transformer uses Self-attention
- Decoder-only Transformer uses Masked Self-attention

## Encoder-Only vs Decoder-Only Transformer

- Encoder-Only transformer: Creates Context Aware Embeddings
  - Context Aware Embeddings are great inputs for creating classification neural network
    - Sentiment Analyis using Softmax
      ![Sentiment Analyis](../images/4_15.png)
    - Classification using Logistic Regression
      ![Classification using Logistic Regression](../images/4_16.png)
- Decoder-Only transformer: Creates Generative Inputs (?? Or should we call it Outputs)
![Encoder-Only vs Decoder-Only Transformer](../images/4_13.png)
  - Generative inputs can be plugged into a simple Neural Network to generate new tokens
    ![Generate new tokens](../images/4_14.png)
  - Also called **Generative Model**
  - These models are good at text generation because they are specifically trained to generate text that comes after a prompt.
