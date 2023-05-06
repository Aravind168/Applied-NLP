### Tasks

1. Created a vocabulary from training data with a threshold count of 3. 
2. Constructed a HMM with transition and emission probabilities by parsing training data.
3. Performed greedy decoding by selecting the most likely state for the first word, and then used that to decode maximize P(s2|s1) to continue to choose local optimal value (local maxima). Achieved an accuracy of 91.85% on the dev data.
4. Performed Viterbi decoding using the Viterbi matrix and backpointer matrix. Once the Viterbi matrix is calculated using the formula, the best path is constructed backwards by selecting the maximum probability value in each column of the Viterbi matrix. Achieved an accuracy of 93.23% on the dev data.
