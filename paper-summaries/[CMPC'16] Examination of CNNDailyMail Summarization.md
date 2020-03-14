# An Examination of the CNN/DailyMail Neural Summarization Task

> **Authors:** Vincent Chen, Eduardo Torres Montano, Liezl Puzon, Danqi Chen
>
> **Published:** 2016
>
> **Source:** https://web.stanford.edu/class/archive/cs/cs224n/cs224n.1174/reports/2762104.pdf



## Introduction / background

### CNN/DailyMail dataset

- Each article is paired with a short set of summarized bullet points that represent meaningful highlights of the piece.
- At 2016, the state-of-the-art (SOTA) is >35% by [Nallapati et al.](https://www.aclweb.org/anthology/K16-1028/), which trained a hierarchical attention model for 18 days (35 epochs) on a single Tesla K-40 GPU. 
  - The entire input article was used for training with 4 bullet points as gold labels. 
- In contrast, this work will only use the first two sentences of each article. This is an effective and efficient use of the dataset since big ideas are often communicated early on in news articles. Only one bullet point will be used as the gold label.
  - Non-neural extractive techniques can also be used to find the most salient sentences in an article for training ([LexRank](https://pypi.org/project/lexrank/)).

### Extractive vs abstractive summarization

- **Extractive:** concatenation of extracts from the source corpus.
- **Abstractive:** generates and paraphrases sentences to capture salient points of an article.

**Abstractive text summarization.** As of 2016, the SOTA is to use neural attentive encoder-decoders.

- [Chopra et al.](https://www.aclweb.org/anthology/N16-1012/) uses a deep convolutional encoder and a beam-search decoder, trained on 4M article-summary pairs from the Gigaword dataset. It was a continuation of work from [Rush et al.](https://www.aclweb.org/anthology/D15-1044/) (2015).
- [Nallapati et al.](https://www.aclweb.org/anthology/K16-1028/) uses a bidirectional GRU-RNN encoder, unidirectional GRU-RNN decoder with attention and the [large vocabulary trick](https://medium.com/@xuy/handling-rare-words-in-machine-learning-models-89e472ce8519). 

### Encoder-decoder structure

- An encoder is an RNN that turns an input sequence into a different representation
- A decoder has a similar structure to an encoder, but instead tries to generate a word that best corresponds to its hidden state. Runs until it reaches the end of its inputs, at 30 words, or if it generates an End-of-sentence (`<EOS>`) token.

## Approach



