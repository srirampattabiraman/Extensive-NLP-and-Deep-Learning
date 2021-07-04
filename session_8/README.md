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

With the help of custom function called **yeild** that has iterable object and language as an argument and returns the list of tokens

Following are the special tokens used

UNK_IDX --> Unknown token
PAD_IDX --> Padding token
BOS_IDX --> Beginning of string
EOS_IDX -- End of string





