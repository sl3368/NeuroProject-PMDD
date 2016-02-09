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

#2016-02-08

I have been working on generating optimal stimuli for our trained 
networks for multiple different models. Some of the analysis done 
was looking at specific neurons which were estimated poorly by GLM 
and attempting to extract what was learned by using non-linear models
for these neurons. The results showed some differences in the findings, 
but the issue is that the optimal stimuli is difficult to visually 
interpret. One of the very interesting outcomes was the close resemblence 
to a whole song when generating the optimal stimuli for all the neurons 
in a single brain region. After discussing with Josh, decided that it would 
be good to pursue this with aggregation of all other regions which data 
has been collected upon. Hopefully we can move closer and closer to the full 
song, difficult to interepret biologically though.

Other progress made: working on different aspect of the project which deals 
with a data set from the retina of primates. This has been trained by other 
members of the group, but seems to be successful in using non-linear models
(big improvement over GLM). Task here is applying a lot of the analysis methods 
from the song data to this set of models. Additionally, the story must be consistent 
with that of previos neurological findings about the type of cells that exist 
in the area.

-Working on getting our third (and final) data set, which is in a higher brain 
region. This is neuron firing from natural images (rats and primates). Liam is 
in talks with collaborators, should hopefully have this soon.

-While reading more about Bayesian non-parametrics, an idea came to me about 
using this in conjunction with VAE to work as a flexible image classifier. 

-Working on understadning Kingma's code to attempt hashing out this idea, 
need to work out inference with the CRP.
