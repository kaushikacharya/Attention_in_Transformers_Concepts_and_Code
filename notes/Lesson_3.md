# Coding Self-Attention in PyTroch

- `nn.Module`
  - Base class for making all neural network modules in PyTorch
- Batch size
  - Usually it is the first dimension
  - But we won't use in this example
- Bias terms
  - Additional bias terms were not present in the original Transformers mannuscript
- `nn.Linear`
  - Along with storing the **Weights**, it also does the math
- **forward()**
  - Calculation of **Self-Attention** values for each token happens in this function
  - **token_encodings**
    - This input parameter contains the token encodings
    - These are the **Word Embeddings** plus **Positional Encoding** for each input token

## Notebook

- [Jupyter Notebook](../code/Lesson_3.ipynb)
- Why are weights transposed during print?
  - In [nn.Linear](https://pytorch.org/docs/stable/generated/torch.nn.Linear.html) the weights are of shape ($out\_features,in\_features$).
