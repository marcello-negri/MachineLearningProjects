## Predict proprieties of a protein based on its shape (final grade 6/6)

### Challenge
We are given a train set of proteins represented as strings of 4 letters, which enccode the information of the amino acids they are made of. Each protein is linked to a ground truth value of either 0 or 1 representing whether the protein is active or inactive, respectively. The aim of the project was to predict if previously unseen proteins of the test set were active or inactive. 

### Solution
The key idea to solve the problem consisted in properly expressing the information relative the four amino acids that form the protein. In particular, we encoded the information of a single amino acid into a vector of length 21 (the total number of amino acids) with all zero entries except for one, which then represents uniquely the amino acid. In order to express a sequence of four amino acids we concatenated 4 vectors of length 21, which then clearly expressed the composition of the protein. At this point we exploited a neural network, optimised through cross validation, to perform the classification problem. Interestingly, the result were already optimal even before optimising the neural netwrok, suggesting the key idea behind the problem was **data preprocessing**.
