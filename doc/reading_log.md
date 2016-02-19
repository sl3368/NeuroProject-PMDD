# 2016-01-29 Bengio et al., 2003.

First off, I was very impressed by this work. The use of neural networks, and especially deep neural networks,
have only recently become popular. Having worked with them, they can be a significant engineering challenge.
To have wrestled with such a model with the tools (languages, packages, etc.) and more importantly, computational 
resources, that existed over a decade ago is extraordinary. As for the model itself, it is well thought out and 
logically proposes to improve on traditional n-gram models. It is a good predecessor to some of the more 
complex word embedding models that have been proposed more recently (i.e. word2vec or GloVe). For me, the paper 
elucidated why word embedding models are much better at generalizing in this extremely high dimensional space. 
I believe this is can be an important point when considering similar types of problems.

Talking points:
- Distributed Representations are a much better way to model this high dimensional data, can generalize

- The authors propose using a MLP (with softmax) to predict the ith word given the context 

- How do this model compare to more recent word embedding models?

- Can this be improved upon using more advanced non-linear models such as RNNs?

- They discuss polysemous words would not be captured well (since single point), how 
could this model be improved?

- What other domains could this potentially be applied towards? (Cheminformatics maybe)


# 2016-02-02 Mikolov et al., 2013.

I am not convinced that the analogies task (this is the same as word similarity?) is a good metric for measuring 
how well inferred these word vectors are. Though this may be good for language modelling (predicting whether a 
combination of words is valid), I think the crux of this problem is inferring semantic definitions of words 
themselves. Of course this difficult since definitions are dependent on words themselves. That being said, this 
task takes into account syntax, word tense, and other components which make it difficult to infer real semantic 
definitions of words.

-I understand the hierarchical softmax mathematically, but does that mean the output of the softmax is a binary 
vector of size log(N)?

-The idea of negative sampling was thoroughly confusing to me, I do not understand why this can replace the log 
probability term in the skip gram objective. 

# 2016-02-03 Pennington et. al., 2014.

I liked the explanation of the authors intuition in this paper. It was similar to the first Bengio paper which we read. 
It pin points that co-occurence is the basis of all information for inference. Adjusting the context 
for this co-occurence can deeply affect the qaulity of understanding. This makes sense intuitively, if 
all our minds could only process words with a memory of a few words before and after, it would be difficult 
to ultimately gain an understanding of low frequency words. 

-I am curious whether increasing the context window to be very large in the skip-gram model (and taking the time 
to train something that large) would result in a model of similar accuracy to GloVe.

-Essentially, is this a matter of drawing from a different information source, or does the actual difference in 
objectives cause better embedding performance?

# 2016-02-03 Arora et al., 2015.

This was a novel way of looking at the word embedding task, and it was interesting how the random walk novel 
was framed in the context of a generative process. Although a lot of the finer details were difficult for me to 
comprehend, I especially liked how the authors compared this models to the GloVe and Word2Vec models we read 
about earlier.

# 2016-02-18 Arora et al., 2016

This was an interesting paper which aimed to investigate one of the flaws with traditional word vectors: 
polysemy. The authors describe an experiment in which they combine two random words, and create a new 
word using the occurrences of these two words in a text. This is a good way of artificially creating 
these new words. In the experiment, the authors find that " it allows the less dominant/frequent sense 
to have a superproportionate contribution to v_new , thus making it detectable in principle despite 
noise/error". I was not quite sure how to interpret this finding.

-Is this just a result of the model used in the previous paper?

-With all these experiments on language modelling and word vectors, how are the results not highly 
dependent on the corpus. Although these corpora are sufficiently large, the size of the vocabulary would seem
prohibitive to making generalizations to all text. 


# 2016-02-18 Le et al., 2016

This paper was an extension of the conversation we've been having regarding word vectors. The authors of the paper 
propose an unsupervised method for learning vector representations of paragraphs. The definition of a paragraph 
can be of any size (sentence, paragraph, or document). The model the authors propose is a concatenation of a fixed 
sized context of words (to predict the next word) along with the paragraph vector, which acts a long term memory. 
The authors seem to keep the word vectors fixed. I liked the distributed bag of words method also discussed. 

-I am curious what would happen if models with recurrence were used for this representation. There has been a lot of 
work on predicting the sequence of words, and in fact, there was a recent paper this summer that took conversations 
and was able to perform well in predicting the appropriate response using these aforementioned models. For example 
what if an LSTM were trained on attempting to predict the next word vector in a paragraph, and the final output 
vector for this was a paragraph vector?

# 2016-02-18 Levy et al., 2016

I did liked how these authors made a deep theoretical connection between models. It seems in reading different 
works in the machine learning space, a large portion of the efforts results in proposing a model based on some 
assumptions and then showing its "state of the art" performance on some known data set. With little discussion 
on why the model works better, how it theoretically compares to others, and what may be a different theoretical 
approach that would obtain vastly different results. I  appreciated how this paper made the link between the 
skip gram negative sampling model and matrix factorization. I did not understand this proof entirely, but it is 
nice to see the connection between the two models and how they are optimizing the same objective.
