# 2 Regularizing your Neural Network

If you suspect your neural network is `over-fitting` your data -> you have `high variance`:
- One of first thing you should try probably is regularization.
- The other way to address `high variance` is to get more training data. That is also quite reliable. But you can't always get more data, or it could be expensive to get more data.

## Regularization

[**Logistic Regression**](PENDING)
**Need to relearn ML to understand it  :( **

$$\[
\min_{w, b} J(w, b)
\]$$

Try to minimize the cost function $\( J(w, b) \)$.

$$\[ J(w, b) = \frac{1}{m} \sum_{i=1}^{m} \mathcal{L}(\hat{y}^{(i)}, y^{(i)}) + \frac{\lambda}{2m} ||w||^2 \]$$

$$ \text{where } ||w||^2 = w^T w = \sum_{j=1}^{n_x} w_j^2 $$

- $||w||^2$ is L2 regularization, because here are using Euclidean norm, also it's  called the L2 norm with the parameter $w$.



Please note that in the next video at 5:45, the Frobenius norm formula should be the following:

$$\[
||w^{[l]}||^2 = \sum_{i=1}^{n^{[l]}} \sum_{j=1}^{n^{[l-1]}} (w_{i,j}^{[l]})^2
\]$$

The limit of summation of $\( i \)$ should be from 1 to $\( n^{[l]} \)$,

The limit of summation of $\( j \)$ should be from 1 to $\( n^{[l-1]} \)$.

(it's flipped in the video). The rows $i$ of the matrix should be the number of neurons in the current layer $\( n^{[l]} \)$;

whereas the columns $j$ of the weight matrix should equal the number of neurons in the previous layer $\( n^{[l-1]} \)$.
