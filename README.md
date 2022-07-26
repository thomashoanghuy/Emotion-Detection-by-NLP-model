# Emotion-Detection-by-NLP-model
Emotion Detection by NLP model (RoBERTa)
1 | P a g e
Introduction
With the advance of technology, available information online and the abillity to perform more and more banking tasks digitally whereever the customer is at, manag people no longer visit bank branches anymore. While the proliferation of digital banking has improved efficienct and convenience for the customer, it has also eliminated some of the face to face interaction opportunities banks previoulsy had with their customers. Custmers still have many occasions when it is necessary to talk to a bank officer and during those occasions, both banks and their customers wish to have a positive experience. 

Chatbots comes in handy to redefine the banking experience in these case. Chatbots have the potential to reshape user expectations and desires when banking. With chatbot’s numorious benefit bring to the banks, it could also lower customer satisfaction or loyalty with its missing interpersonal communication skills. As it is, many incoming calls result not from an initial preference for live assistance, but out of frustration with the inadequacy of the automated version. This has lead to our problem statement, can emotion analysis detect unsatisfied customers in chat before they turn towards human assistance?


In this research we will be building a emotional analysis model on public tweets, trying to understand the underlying emotions in the tweets and use this model to identify customer emotions in their query to the banks chatbot and flag cnoversations when the customers are unsatified with the chatbot and request for human interventions.


In 2018, the BERT (Bidirectional Encoder Representations from Transformers) model for Natural Language Processing was developed by the researchers at Google Research. 

BERT works with the help of Transformers, which is an attention mechanism designed to learn contextual relations between different words or sub-words in any given text. 

Transformers, in its most basic form, utilizes two separate mechanisms: an encoder to read the text input, and a decoder to make a prediction for the given task. 

Given that the generation of a language model is BERT's goal, the encoder mechanism is sufficient. Unlike directional models, BERT does not read the text input sequentially (either left to right or right to left). Instead, it reads the entire word sequence at once. Therefore, it is considered 'bidirectional', although 'non-directional' is a better word to explain its working principle. 
This is more efficient, since it makes it possible for the model to learn the context of a word by considering all the matter that surrounds it.


i. Pre-training

Pre-training involves training the model on unlabelled data over different pre-training tasks.
- Masked LM: Some percentage of the input tokens masked at random, and then those masked tokens are to be predicted.
- Next Sentence Prediction: Downstream tasks such as Question Answering (QA) and Natural Language Inference (NLI) are based on understanding the relationship between two sentences, which is not directly captured by language modelling. A binarized next sentence prediction task is pretrained that can be trivially generated from any monolingual corpus.
- Pre-training Dataset: BERT can be trained on different Datasets depending on the downstream tasks.
ii. Fine-tuning




The results of the above application proves the model works quite well in many different contexts. However, we also idfentified certain levels of limitations.

5.1 Text-only limitation
The data sources are mainly in text-only based, which lacks of tones, face motion and other body languages. This will cause three potiential issues:

• Syntactic: This means it’s possible that same words can represent different meanings as well as different emotions. For example, “Lie” can be “untruth” but also can be “lay down”. This brings us some troubles during the encoding process

• Semantics: We are analysing the data without context, and the sentence input is one by one. It’s not linked to backwards and forwards.

• Sarcastic: Masked meaning. People may use speak certain sentences but totally opposite meanings.

5.2 Model-level limitation

• BERT Model: The model we are using is not portable, which means it consumes lots of computing power.

• Sentence Maximum Length: There is max. Length of sentence to input.

• Complicated emotions: The current output is showing one output with multiple confidence levels.
