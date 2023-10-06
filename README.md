## icr-identifying-age-related-conditions
## got a score better than the winner.
![icr-iarc-submission](https://github.com/bishnarender/icr-identifying-age-related-conditions/assets/49610834/8df9e745-38cb-4777-9dc8-60f6be161fb1)

### Start 
-----
For better understanding of project, read the files in the following order:
1. eda.ipynb 
2. training.ipynb
3. icr-iarc-submission.ipynb

### Model
-----
![identify_age](https://github.com/bishnarender/icr-identifying-age-related-conditions/assets/49610834/218e65e3-167f-4783-9649-9d7ba5cb65ed)

56 in Input [BS,56] is our "anonymized health characteristics".

Dropout is not used.

Using factor=0.95 in ReduceLROnPlateau had kept the difference between train_loss and val_loss high i.e., reducing learning_rate sharply was making the model unstable. So, I kept factor=0.999 which provided me with a "train_loss and val_loss" set with less difference such as [0.1455, 0.1582].

Smish activation is computed as <b>smish(x)=x⋅tanh(ln(1+σ(x)))</b>.

Reweighting the probabilities in the submission worked well.
