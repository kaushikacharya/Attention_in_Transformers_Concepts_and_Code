# Coding Masked Self-Attention in PyTorch

## Notebook

- [Jupyter Notebook](../code/Lesson_6.ipynb)
- **Observation**
  - Though the [theory of masked self-attention](./Lesson_5.md) shows mask matrix being added to scaled similarity matrix, but in implementation the masked values are modified using $masked\_fill$ function.
