# Machine Translation

Translating a text from One Language To Another.

<br>
<img src ="images/image.jpg"  width=800 height=500>  
<br>

## Methods Used

1. Encoder - Decoder Architecture

2. Attention Mechanism

2. Training and Inference Mode of Decoder

## Encoder-Decoder Architecture

1. The encoder LSTM is used to process the entire input sentence and encode it into a context vector, which is the last hidden state of the LSTM/RNN. This is expected to be a good summary of the input sentence. All the intermediate states of the encoder are ignored, and the final state id supposed to be the initial hidden state of the decoder.

2. The decoder LSTM or RNN units produce the words in a sentence one after another. The model is trained by Teacher Forcing technique and tested through the Inference mode.

## Attention Mechanism

In psychology, attention is the cognitive process of selectively concentrating on one or a few things while ignoring others. The attention mechanism was born to help memorize long source sentences in neural machine translation (NMT). 

Rather than building a single context vector out of the encoder's last hidden state, the secret sauce invented by attention is to create shortcuts between the context vector and the entire source input.

## Bahdanau Attention

1. Producing the Encoder Hidden States - Encoder produces hidden states of each element in the input sequence.

2. Calculating Alignment Scores between the previous decoder hidden state and each of the encoder’s hidden states are calculated (Note: The last encoder hidden state can be used as the first hidden state in the decoder).

3. Softmaxing the Alignment Scores - the alignment scores for each encoder hidden state are combined and represented in a single vector and subsequently softmaxed.

4. Calculating the Context Vector - the encoder hidden states and their respective alignment scores are multiplied to form the context vector.

5. Decoding the Output - the context vector is concatenated with the previous decoder output and fed into the Decoder RNN for that time step along with the previous decoder hidden state to produce a new output.

6. The process (steps 2-5) repeats itself for each time step of the decoder until an token is produced or output is past the specified maximum length.

<br>
<img src ="images/image1.jpg"  width=800 height=500>  
<br>


# Technologies Used
```
1. LSTM

2. GRU

3. Sequence To Sequence Model(Encoder-Decoder)

4. Bahdanau Attention Mechanism

```

## Usage

It can be used as a translator where you will be getting the result in a new language.

## Improvement

We can improve the model by improving the dataset. Training with more epochs with the improved dataset.

### Author 
```
Rahul Kumar Patro
```


