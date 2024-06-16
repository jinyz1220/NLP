## Pretrained Language Models for Classification

### Overview
This project involves exploring and fine-tuning pre-trained language models for classification tasks using the HuggingFace Transformers library. The primary focus is on the masked language model BERT (Devlin et al., 2019), with additional experiments using the autoregressive language model GPT-2 (Radford et al., 2019) for extra credit.

### Objectives
1. **Classification with BERT [CLS] Features**: Implement a classifier using the [CLS] token from BERT.
2. **Classification with Mean-Pooling and Max-Pooling**: Implement classifiers using mean-pooling and max-pooling of BERT representations.
3. **Comparison of Pooling Techniques**: Compare the effectiveness of different pooling techniques.
4. **Fine-tuning BERT**: Fine-tune the BERT model, modifying the parameters of the last two layers.
5. **Extra Credit: GPT-2**: Implement GPT-2 as a feature extractor for classification tasks.

### Provided Data
- **Training, Development, and Test Sets**: Provided for classification tasks.
- **Pretrained Word Embeddings**: 50-dimensional skip-gram word embeddings trained on a large corpus of English tweets.

### Implementation Steps

#### 1. Classification with BERT [CLS] Features
1.1 **Model Implementation**
- Implement a ReLU-activated 2-layer perceptron classifier with a hidden layer size of 32.
- Use the 768-dimensional [CLS] token from `bert-base-cased` as input.
- Train the classifier for 1 epoch with a learning rate of 0.0005 and a mini-batch size of 32.
- Keep BERT parameters fixed and only optimize the classifier parameters.

1.2 **Evaluation**
- Run the experiment 5 times with different random seeds.
- Report mean accuracy and standard deviation on the development set.
- Report accuracy on the test set for the best-performing model.

#### 2. Classification with Mean-Pooling and Max-Pooling
2.1 **Model Implementation**
- Implement classifiers using mean-pooled and max-pooled BERT representations of content tokens.
- Train the models for 1 epoch with the same hyperparameters as in 1.1.
- Ensure padding tokens are not considered as content tokens.

2.2 **Evaluation**
- Run the experiments 5 times with different random seeds.
- Report accuracy and standard deviation on the development set.

#### 3. Comparison of Pooling Techniques
3.1 **Analysis**
- Compare the effectiveness of first-token, mean-pooling, and max-pooling techniques based on the results from the previous experiments.

#### 4. Fine-tuning BERT
4.1 **Model Implementation**
- Fine-tune BERT by modifying the parameters of the last two layers (layers 10 and 11).
- Use the same classifier and hyperparameters as in 1.1.
- Train and evaluate the model.

4.2 **Evaluation**
- Report accuracy and standard deviation on the development set.
- Compare results with those obtained in 1.1 and 2.1.

#### 5. Extra Credit: GPT-2
5.1 **Model Implementation**
- Implement GPT-2 as a feature extractor for the DBpedia classification task.
- Train and evaluate the model using the same hyperparameters as in previous experiments.

5.2 **Evaluation**
- Report accuracy and standard deviation on the development set.
- Report accuracy on the test set for the best-performing model.
