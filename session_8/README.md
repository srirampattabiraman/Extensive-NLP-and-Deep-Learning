**Text Processing pipeline using torch text**

**Problem Statement**

With the concepts learned we will be refactoring the items 2 and 3 in the [repository](https://github.com/bentrevett/pytorch-seq2seq) by replacing the legacy way of tokenizing with the new approach

**Dataset used**

Multi30k 

**Source**
Torch Dataset module

**Preprocessing Pipeline**

**Tokenizeing** 
**Building vocabulary**
**Data collation**

**Tokenization**

Tokenization is performed by using **get_tokenizer** module that has following arguments

•	tokenizer – the name of tokenizer function. If None, it returns split() function, which splits the string sentence by space. If basic_english, it returns _basic_english_normalize() function, which normalize the string first and split by space. If a callable function, it will return the function. If a tokenizer library (e.g. spacy, moses, toktok, revtok, subword), it returns the corresponding library.
•	language – Default en

**Building Vocabulary**

With the help of custom function called **yeild_token** that has iterable object and language as an argument and returns the list of tokens

Following are the special tokens used

UNK_IDX --> Unknown token
PAD_IDX --> Padding token
BOS_IDX --> Beginning of string
EOS_IDX -- End of string

**build_vocab_from_iterator**  method with tokenized data from multi30k dataset and special tokens in hand returns vocuablary objects for desired languages.

**Models architecture**

Learning_Phrase_Representations_using_RNN_Encoder_Decoder_for_Statistical_Machine_Translation.ipynb ---> uses GRU

Neural_Machine_Translation_by_Jointly_Learning_to_Align_and_Translate.ipynb ---> uses attention mechanism

**Data Collation phase**

Data iterator yields a pair of raw strings. 
We need to convert these string pairs into the batched tensors that can be processed by our ``Seq2Seq`` network 
defined previously. Below we define our collate function that convert batch of raw strings into batch tensors that
can be fed directly into our model.   

**Train Logs**

**Learning_Phrase_Representations_using_RNN_Encoder_Decoder_for_Statistical_Machine_Translation**

![image](https://user-images.githubusercontent.com/55537646/124389037-05fc6700-dd03-11eb-9961-ff35a86d3cab.png)


**Neural_Machine_Translation_by_Jointly_Learning_to_Align_and_Translate**

![image](https://user-images.githubusercontent.com/55537646/124389120-64c1e080-dd03-11eb-8875-0b79bf7d3fa8.png)

While working on 
**Packed Padded Sequences, Masking, Inference and BLEU**

I Got below error
RuntimeError: 'lengths' argument should be a 1D CPU int64 tensor, but got 0D cpu Long tensor

it is not accepting source length to cpu device, as per the suggestion downgrading torch seems to be giving expected results





