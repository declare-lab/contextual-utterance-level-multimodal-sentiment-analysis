## Context-Dependent Sentiment Analysis in User-Generated Videos
Code for the paper [Context-Dependent Sentiment Analysis in User-Generated Videos](http://sentic.net/context-dependent-sentiment-analysis-in-user-generated-videos.pdf) (ACL 2017).

### Requirements
Code is written in Python (2.7) and requires Keras (2.0.6) with Theano backend.

### Dataset
We provide results on the [MOSI dataset]{https://arxiv.org/pdf/1606.06259.pdf}

Please cite the creators 

### Input Formatting
As data is typically present in utterance format, we combine all the utterances belonging to a video using the following code

```
python create_data.py
```

Note: This will create speaker independent train and test splits 

### Training sc-lstm

Sample command:

```
python lstm.py --unimodal True
python lstm.py --unimodal False
```

Note: Keeping the unimodal flag as True (default False) shall train all unimodal lstms first (level 1 of the network mentioned in the paper)

Note: Unlike the paper, we haven't used an SVM on the penultimate layer. This is in effort to keep the whole network differentiable at some performance cost.

### Developers

#### Devamanyu Hazarika
email: devamanyu@u.nus.edu
Ph.D. Researcher at NUS, Singapore

#### Soujanya Poria, Ph.D.
email: 


