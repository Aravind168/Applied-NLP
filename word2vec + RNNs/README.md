### Tasks

1. Generated TF-IDF and word2vec features for Amazon Reviews. Compared the performance of both features to perform multi-class classification using Perceptron and SVM. Observed better accuracies using TF-IDF. This could be because word2vec was trained on a wide context that may not have seen all these emotions to weigh them well in vector space. 

2. Implemented custom dataset classes and inherited dataloaders to enable training on PyTorch.

3. Implemented MLP and analyzed how to feed features to model. Tested with 2 ways:
    i. Average all vectors to generate a vector of same dimension for review
    ii. Concatenate the first 10 words to generate a vector of higher dimension for review.
Observed that in the second case, the training loss decreases while validation loss increases. Experimented with dropout and lower learning rates but this phenomenon seems to occur regardless. The MLP performs significantly better than a single perceptron. Adding complexities to the model with non-linearity and layers has improved the performance from 48% to 66.1% in the first case. The disparity between the two cases is possibly because the first case tries to capture the entirety of a review while still maintaining lower dimensions whereas the latter concatenates the first 10 words, which may not contain all necessary information to classify, and also increases the dimensions of features.

4. Implemented vanilla RNN, GRU, and LSTM and compared the performance of these models on the same classification task. GRU offers significant improvement over RNN due to the mechanism of gates that are capable of learning which inputs are important and need to be remembered. This additional gate mechanism solves the vanishing gradient problem of RNN but is causing the GRU to overfit on training data. LSTM is computationally slightly more expensive than GRU and offers solutions to the problem of overfitting by adding a forget gate. This results in better performance in both training and validation data.

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
