---
attachments: [Clipboard_2022-03-11-13-13-16.png, Clipboard_2022-03-11-13-27-31.png, Clipboard_2022-03-11-13-29-25.png]
tags: [Notebooks/NLP/Ngrams]
title: Ngrams and Probabilities
created: '2022-03-11T07:41:08.473Z'
modified: '2022-03-12T10:45:34.285Z'
---

# Ngrams and Probabilities

Sequence notation

![](@attachment/Clipboard_2022-03-11-13-13-16.png)

- w1, w2, w3 . . .wn denotes different words
- To refer sequecnce of words from 1st to w3 we can use $w_1^3$ = $w_1 w_2 w_3$

#### Unigram probability
**Corpus : I am happy because I am learning**
- Size = 7
- $P(I) = 2/7$
- $P(Happy) = 1/7$

![](@attachment/Clipboard_2022-03-11-13-27-31.png)

#### Bigram probability
**Corpus : I am happy because I am learning**
- $P( am /I ) = count ( I  am) / count ( I )$

![](@attachment/Clipboard_2022-03-11-13-29-25.png)


