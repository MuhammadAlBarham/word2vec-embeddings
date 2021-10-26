# word2vec algorithm using skip-gram architecture

## Why to use Embedding layer instead of one-hot encoding?

If you using one-hot encoding you will end up with a lot zeros at the hidden out of the first hidden layers. 
To solve this problem, an embedding layer used as a lookup table.

The words are encoded as integers that used as index for words in the lookup table. for example, "go" might be encoded as 148
and it means that it corresponds to the 148th row of the embedding matrix.

- The rows of the matrix are corresponds to the number of words.
- The columns of the matrix are corresponds to the hidden dimension.

## word2vec

**Word2Vec** uses the embedding layer to find vector representations of words that contain semantic meaning(relating to meaning in language or logic.
).

## Loading data and pre-processing:


** Here I'm fixing up the text to make training easier. This comes from the utils.py file. The preprocess function does a few things:

- It converts any punctuation into tokens, so a period is changed to <PERIOD>. In this data set, there aren't any periods, but it will help in other NLP problems.
- It removes all words that show up five or fewer times in the dataset. This will greatly reduce issues due to noise in the data and improve the quality of the vector representations.
- It returns a list of words in the text.

Then, to reduce th noise from our data and to get better training and representation, subsampling is used.

  
## Do we need all layers of the network?
  
It depends on the application but for this application we need embedding layers only (as a lookup table).
 
The image below shows a network for input, embedding and output layer. We only need the embedding layer.
  
![a](https://github.com/MuhammadAlBarham/word2vec-embeddings/blob/9f2d9e83896630355afb0af992abaaab8122f71c/assets/skip_gram_arch.png)
  
 
 ## Validation
  
  The validation is done by cosine similarity.
 
 ## Visualization for the results
  
  
  
  
