# 2016-01-29

Worked on texture gradients method for neuron decoding.

#Project Plan

-Clean and format data appropriately

-Perform Gaussian smoothing analysis

-Build convolutional neural net with time series model

-attempt using variational rnn described by bengio et al

-Select poorly predicted neurons by GLM and do select analysis

-Write project report


#2016-02-02

We are discussing with collaborators on final details of the 
visual stimuli data set. In the meantime I have been wrapping up 
work on the bird song data set. It seems as though although there 
are neurons which have non-linear activations, but it is not quite 
clear how well they are modelled by the LSTM architecture we are 
using. Though the hypothesis we initially had was not confirmed 
by the data set we were working with, some good processes were developed 
for highlighting neurons with non-linear behavior. 

#2016-02-03

One of the final comparisons which I have been working on with the 
bird song data set is to use texture generation with learned model 
parameters to reconstruct the original song. I have isolated 
neurons which are being predicted poorly by the GLM and  
trained a model for just these neuron which did not perform worse 
than the much larger with all the data. This begs the question 
as how much information from the input was used in the neurons that 
were well predicted by the GLM. By looking at the difference in the 
generated song by both models, some insights could be gained 
regarding the information captured in these different neuron sets.
