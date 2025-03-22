# The Matrix Math for Calculating Masked Self-Attention

- Self-Attention vs Masked Self-Attention Equation
  ![Masked Self-Attention Equation](../images/5_0.png)
- Purpose of mask
  - Prevent tokens from including anything that comes after them when calculating attention
- Mask value $-inf$ applied
  ![mask value](../images/5_1.png)
  - $-inf$ converts masked tokens' softmax value to 0
- Masked self-attention is reflected on the value computation
  - Only previous tokens have influence
  ![Masked self-attention scores](../images/5_2.png)
