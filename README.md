# Attention in Transformers: Concepts and Code in PyTorch

## About

This repository contains

- [Course notes](#course-contents)
- [Assignments](#assignments)
- Additional resources (collected for better understanding of the concepts)

## Course Information

- Instructor: Josh Starmer
- [Course Website](https://www.deeplearning.ai/short-courses/attention-in-transformers-concepts-and-code-in-pytorch/)

## Course Contents

|#|     Lesson  |   Description   |
|-|-------------|-----------------|
|0|[Introduction](./notes/Lesson_0.md)|<ul><li>Challenges in earlier approaches of Machine Translation</li><li>History of Attention Mechanism</li><li>Models evolved from Encoder and Decoder</li><li>Course outline</li></ul>|
|1|[The Main Ideas Behind Transformers and Attention](./notes/Lesson_1.md)|<ul><li>Three main parts of Transformers</li><li>Self-attention explained with an example</li></ul>|
|2|[The Matrix Math for Calculating Self-Attention](./notes/Lesson_2.md)|<ul><li>Query, Key, Value explained in terms of Database Management Systems</li><li>Computation of Queries, Keys and Values</li></ul>|
|3|[Coding Self-Attention in PyTroch](./notes/Lesson_3.md)|<ul><li>Create a basic Self-Attention class</li></ul>|
|4|[Self-Attention vs Masked Self-Attention](./notes/Lesson_4.md)|<ul><li>Word Embeddings: Trained via next word prediction using previous word(s) as context</li><li>Encoder-only model: Context aware embeddings</li><li>Decoder-only model: Generative inputs</li><li>Self-Attention vs Masked Self-Attention</li></ul>|
|5|[The Matrix Math for Calculating Masked Self-Attention](./notes/Lesson_5.md)|<ul><li>Self-Attention vs Masked Self-Attention Equation</li><li>Mask value $-inf$</li></ul>|
|6|[Coding Masked Self-Attention in PyTorch](./notes/Lesson_6.md)|<ul><li>Create a basic Masked Self-Attention class</li></ul>|
|7|[Encoder-Decoder Attention](./notes/Lesson_7.md)|<ul><li>Encoder-Decoder Attention, aka Cross-Attention in Seq2Seq model</li><li>Relevance in Multi-Modal models</li></ul>|
|8|[Multi-Head Attention](./notes/Lesson_8.md)|<ul><li>Combine attention values from multiple heads via fully connected network to output attention values same as single head attention</li><li>Alternative approach of reducing weight matrix columns</li></ul>|
|9|[Coding Encoder-Decoder Attention and Multi-Head Attention in PyTorch](./notes/Lesson_9.md)|<ul><li>Implemented Encoder-Decoder Attention and Multi-Head Attention</li></ul>|
|10|Conclusion|<ul><li>Summarizing the 3 different Attention studied in the course</li></ul>|

## Assignments

  |Lesson|         Assignment        |   Description   |
  |-------|---------------------------|-----------------|
  |#3|[Coding Self-Attention in PyTroch](./notes/Lesson_3.md#notebook)|<ul><li>Create a basic Self-Attention class.</li><li>Verify calculations.</li></ul>|
  |#6|[Coding Masked Self-Attention in PyTorch](./notes/Lesson_6.md#notebook)|<ul><li>Create a basic Masked Self-Attention class</li></ul>|
  |#9|[Coding Encoder-Decoder Attention and Multi-Head Attention in PyTorch](./notes/Lesson_9.md#notebook)|<ul><li>Extended above classes with Encoder-Decoder Attention and Multi-Head Attention</li></ul>|

## Certificate

- [Course Completion Certificate](https://kaushikacharya.github.io/assets/certificates/DeepLearning_ai_Attention_in_Transformers_Concepts_and_Code.pdf)
- Issued on Mar 2025

## Related Courses

Please visit my [Github page](https://kaushikacharya.github.io/courses/#machine-learning--deep-learning) for other Deep Learning courses.
