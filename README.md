# TensorFlow_ChatBot
An implementation of Seq2seq chatbot. [read the technical report] (https://docs.google.com/gview?url=http://sudongqi.com/Documents/2016_02.pdf&embedded=true)

###Features
* dynamic rnn with smart loader
* beam search on prediction
* signal indicator for decoder

###Python 2.7 dependency
* tensorflow 0.12
* numpy
* json

###Instruction
* run "python train.py"
* after training is completed, a model folder will appear inside the data folder
* run "python test.py" to see the result

###Try your own data
it's possible to run it on your own data, but you need to generate at least 2 files with the same format like those in bbt_data.
* text.txt      (required), this is the training data contatining the pair in number token format
* dict.json     (required), this is the dicitonary to translate from number token to English word token in test time
* actors.json   (optional), this is for signal indication in test time
* summary.json  (optional), this file contain the length info for selecting the right bucket options for training

###OpenSubtitles data 
If you want to train on openSubtitles (english 2016) dataset, this tutorial provide a data process script (openSub_data_generator.py) for this format.
[click here](http://opus.lingfil.uu.se/OpenSubtitles2016.php)
