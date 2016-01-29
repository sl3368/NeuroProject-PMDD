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
