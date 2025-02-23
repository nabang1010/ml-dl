# Recurrent Neural Networks - RNN

## Why sequence models
Example of sequence data:
- Speech recognition: x is the audio clip over time and y is a sequence of words
- Music generation: x is the set of notes played and y is the set of notes that be generated
- Sentiment classification: x is the set of words in a sentence and y is the number of stars (1-5) rating
- DNA sequence analysis: x is the DNA sequence and y is the protein sequence
- Machine translation: x is a sentence in English and y is a sentence in French
- Video activity recognition: x is a set of frames and y is the label of the activity
- Name entity recognition: x is a sentence and y is the entities

Some cases:
- Input X and output Y are sequences of different lengths or same lengths or only X is a sequence or only Y is a sequence
 
## Notation
**Motivating Example:**
```txt
x: Harry Potter and Hermione Granger invented a new spell.
   x1    x2     x3  x4       x5      x6       x7x8  x9
y: 1     1      0   1        1       0        0 0   0
   y1    y2     y3  y4       y5      y6       y7y8  y9
   
Tx = 9: The length of the input sequence
Ty = 9: The length of the output sequence
Tx = Ty

X(i): is training example i
X(i)<t>: is the t-th element of the input sequence in training example i
Tx(i): is the length of the input sequence in training example i

y(i): is the output sequence for training example i
y(i)<t>: is the t-th element of the output sequence in training example i
Ty(i): is the length of the output sequence in training example i
```

- $X^{(i)(t)}$: is the t-th element of the input sequence in training example i
- $T_x^{(i)}$: is the length of the input sequence in training example i

- $y^{(i)(t)}$: is the t-th element of the output sequence in training example i
- $T_y^{(i)}$: is the length of the output sequence in training example i


**Representation words**

Vocabulary (Dictionary): a list of the words that you will use in your representation

```txt

Vocabulary: [a, and, invented, granger, harry, hermione, new, spell, potter]
Index:      [7, 3, 6, 5, 1, 4, 8, 9, 2]  

```


