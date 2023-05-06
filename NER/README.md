### Tasks

1. Created a vocabulary and tag set for encoding from training data.
2. Wrote a custom dataset class and inherited dataloader for batching in PyTorch.
3. Implemented a BLSTM with 2 embedding layers. The first layer is used to represent vectors for words in vocabulary and the second layer is used to represent vector to denote whether word is capitalized or not. Tested different hyperparameters to achieve 83.55% F1 score on dev data.
4. Implemented a similar BLSTM but utilized GloVe embeddings as its input layer. Improved performance to 84.58% F1 score on dev data.
