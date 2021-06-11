**Problem Statement**

Take the code from session 4 that handled tweet dataset and convert into such a way that
  1.  encoder: an RNN/LSTM layer takes the words in a sentence one by one and finally converts them into a **single vector**.
  2.  this single vector is then sent to another RNN/LSTM that also takes the last prediction as its second input. Then we take the final vector from this Cell.
  3.  and send this final vector to a Linear Layer and make the final prediction. 
  4.  This is how it will look:
        1.  embedding
        2.  word from a sentence +last hidden vector -> encoder -> single vector
        3.  single vector + last hidden vector -> decoder -> single vector
        4.  single vector -> FC layer -> Prediction
   5. The code needs to look as simple as possible, the focus is on making encoder/decoder classes and how to link objects together
   6. Getting good accuracy is NOT the target, but must achieve at least 45% or more
   7. Once the model is trained, take one sentence, "print the outputs" of the encoder for each step and "print the outputs" for each step of the decoder


**Soultion Description**

1.  Encoder Layer
