# Neural_Machine_Translator---Eng_Fra
# Introduction
1. Neural Machine Translation (NMT) is the task of using artificial neural network models for translation from one language to the other.  
2. The NMT model generally consists of an encoder that encodes a source sentence into a fixed-length vector from which a decoder generates a translation.  
3. This problem can be thought as a prediction problem, where given a sequence of words in source language as input, task is to predict the output sequence of words in target language.  
4. The dataset comes from **http://www.manythings.org/anki/**, where you may find tab delimited bilingual sentence pairs in different files based on the source and target language of your choice.  
5. For this project, I will be using French - English language pairs. If you want to use any other language pairs, make sure to import correct Embeddings (For French - English, I have used __glovetwitter27b100dtxt__)

## The Parameters:
1. **BATCH_SIZE** --> Change this to update the batch size during model training. (Recommended to increase, if sufficient GPU Memory is available)
2. **EPOCHS** --> Update this to increase the number of EPOCHS during model training. Generally, EPOCHS of 5-10 is enough.
3. **LSTM_NODES** --> Change this to update the number of LSTM Units.
4. **NUM_SENTENCES** --> Change to increase the number of phrases on which the model trains. Total sentences in dataset is around 220k, increase, only if sufficienct memory is available.
5. **MAX_SENTENCE_LENGTH** --> Max length of an allowed sentence during model training.
6. **MAX_NUM_WORDS** --> Maximum Number of Unique Words to include during model training.
7. **EMBEDDING_SIZE** --> Change this to update the dimensions of the Embedding Vector in the Embedding Layer.
8. **MODEL_NAME** --> Some pre-trained models are uploaded in the following <br>**GOOGLE Drive Link:-** https://drive.google.com/drive/folders/12nA7oyztLAPJWdcyQP8biJEzo4n_N9DG?usp=sharing <br>In case, you don't change any parameters, and need to run the model, without training, download the respective model and save it in the same folder as this .ipynb file.

## MODEL_DESCRIPTION :-
<ul>
  <li>seq2seq_eng-fra.h5 - This model was trained on 20k phrases from the dataset.</li>
  <li>seq2seq_eng-fra_40.h5 - This model was trained on 40k phrases from the dataset.</li>
  <li>seq2seq_eng-fra_50.h5 - This model was trained on 50k phrases from the dataset.</li>
</ul>

# CONCLUSION
I have used **BLEU Scores** for evaluating the model.  
Upon observation, __BLEU Score__ for __seq2seq_eng-fra.h5__ model was found out to be around __63.5%__, which is a pretty decent score for a low scale model. 
**Accuracy Obtained** = 89.9%  
**Val_Accuracy** = 80.3%
