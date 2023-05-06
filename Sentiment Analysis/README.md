### Tasks

1. Preprocessing of Amazon reviews by performing lemmatization, stemming and removal of stop words.
2. Generate TF-IDF features of reviews and performed train-test split of 80-20.
3. Implement multi-class perceptron, SVM, LR, NB classifiers to predict the rating of review from text. Observed that stemming offers best performance in all the models and removal of stop words resulted in a drop in accuracy. 

| Model      | Preprocessing | Accuracy |
| -----------| ---------| ---------|
| Perceptron | Lemmatization   | 61.9%     |
| Perceptron | Lemmatization + Stop word removal   | 58.9%     |
| Perceptron | Stemming   | 63.9%     |
| Perceptron | Stemming + Stop word removal   | 59.5%     |
| SVM | Lemmatization   | 69.3%     |
| SVM | Lemmatization + Stop word removal   | 65%     |
| SVM | Stemming   | 69.5%     |
| SVM | Stemming + Stop word removal   | 65.7%     |
| LR | Lemmatization   | 70.6%     |
| LR | Lemmatization + Stop word removal   | 67%     |
| LR | Stemming   | 71.1%     |
| LR | Stemming + Stop word removal   | 67.3%     |
| NB | Lemmatization   | 67.3%     |
| NB | Lemmatization + Stop word removal   | 65.4%     |
| NB | Stemming   | 67.9%     |
| NB | Stemming + Stop word removal   | 65.5%     |

Experiments are shown in PDF.
