### Tasks

1. Generated TF-IDF and word2vec features for Amazon Reviews. Compared the performance of both features to perform multi-class classification using Perceptron and SVM. Observed better accuracies using TF-IDF. 

2. Implemented custom dataset classes and inherited dataloaders to enable training on PyTorch.

3. Implemented MLP and analyzed how to feed features to model. Tested with 2 ways:
    i. Average all vectors to generate a vector of same dimension for review
    ii. Concatenate the first 10 words to generate a vector of higher dimension for review.
The MLP performs significantly better than a single perceptron. Adding complexities to the model with non-linearity and layers has improved the performance from 48% to 66.1%. 

4. Implemented vanilla RNN, GRU, and LSTM and compared the performance of these models on the same classification task. Observed best accuracy in GRU.

| Model      | Features | Accuracy |
| -----------| ---------| ---------|
| Perceptron | TF-IDF   | 63%      |
| SVM        | TF-IDF   | 70%      |
| Perceptron | Word2Vec | 48%      |
| SVM        | Word2Vec | 65%      |
| MLP        | Avg Word2Vec | 66.1%    |
| MLP        | Concat 10 Word2Vec | 56.1%    |
| RNN        | Word2Vec | 61.4%     |
| GRU        | Word2Vec | 66.8%     |
| LSTM       | Word2Vec | 66.37%     |

Experiments and detailed explanations are shown in PDF.
