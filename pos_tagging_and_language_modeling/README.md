## Neural Networks for Part-of-Speech Tagging

### Overview
This project involves implementing and experimenting with neural networks to perform part-of-speech (POS) tagging on English tweets. The goal is to build and enhance a neural network model that predicts the POS tag of a word based on its context.

### Objectives
1. **Build a Baseline Neural Network**: Create a neural network to predict POS tags using word embeddings and context words.
2. **Enhance with Feature Engineering**: Improve the model with additional features derived from the data.
3. **Utilize Pretrained Embeddings**: Incorporate and fine-tune pretrained word embeddings for better performance.
4. **Explore Neural Network Architectures**: Experiment with different neural network architectures to optimize tagging accuracy.
5. **Advanced Experiments**: Implement and compare recurrent neural network (RNN) taggers for extra credit.
6. **Language Modeling**: Develop a dataset where a smoothed language model outperforms an unsmoothed model on certain sentences.

### Data Files
- **twpos-train.tsv**: Training data (1173 tweets)
- **twpos-dev.tsv**: Development data (327 tweets)
- **twpos-devtest.tsv**: Development test data (327 tweets)
- **orig-train.tsv**: Original unprocessed training data
- **orig-dev.tsv**: Original unprocessed development data
- **orig-devtest.tsv**: Original unprocessed development test data
- **twitter-embeddings.txt**: 50-dimensional skip-gram word embeddings trained on 56 million English tweets

### Steps to Implement

#### 1. Baseline Neural Network Tagger
- **Model**: Train a feed-forward neural network to predict POS tags. The input is the word embedding of the target word concatenated with embeddings of its context words. The network includes a single hidden layer with tanh nonlinearity and a softmax output layer.
- **Evaluation**: Measure tagging accuracy on development and test datasets.

#### 2. Feature Engineering
- **Enhancement**: Add custom features such as special characters, capitalization patterns, and word length to the input embeddings.
- **Evaluation**: Assess the impact of these features on tagging accuracy.

#### 3. Pretrained Embeddings
- **Initialization**: Use pretrained embeddings from the provided file for initializing word vectors.
- **Fine-tuning**: Experiment with updating these embeddings during training.
- **Comparison**: Compare results of fine-tuned embeddings with fixed embeddings.

#### 4. Architecture Engineering
- **Exploration**: Experiment with different neural network configurations, including varying the number of hidden layers, layer widths, and types of nonlinearities.
- **Window Sizes**: Compare results for different context window sizes (w = 0, 1, 2).

#### 5. Advanced Experiments (Extra Credit)
- **RNN Taggers**: Implement and compare RNN-based taggers, including standard RNN, LSTM, GRU, and bidirectional variants.
- **Evaluation**: Measure tagging accuracies on the development test set.

#### 6. Language Modeling
- **Dataset Creation**: Create a dataset where a smoothed language model assigns higher probability than an unsmoothed model for certain sentences.
- **Analysis**: Write out bigram probabilities for both models and show probability calculations for the key sentence.

### Notes
- **Performance**: Use accuracy as the primary metric for evaluating POS tagging.
- **Optimizers**: Experiment with different optimizers like SGD, Adam, etc., to find the best performance.
- **Hyperparameters**: Tune hyperparameters such as learning rate, batch size, and number of epochs for optimal results.
