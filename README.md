# Second_order_HMM_for_typos_correction

This implementation gives a solution to typos correction in texts without a dictionaries. 
In this problem, a state refers to the correct letter that should have been typed, and an 
observation refers to the actual letter that is typed. Given a sequence of outputs/observations 
(i.e., actually typed letters), the problem is to reconstruct the hidden state sequence 
(i.e., the intended sequence of letters). Thus, data for this problem looks like: 

[('t', 't'), ('h', 'h'), ('w', 'e'), ('k', 'm')]


 [('f', 'f'), ('o', 'o'), ('r', 'r'), ('m', 'm')] 
 
 The first example is misspelled: the observation is thwk while the correct 
 word is them. The second example is correctly typed. 
 
The task can be described as a supervised learning problem: when we see a word, 
for each obseverd letter, we want to predict which letter is most likely to be the 
correct letter. HMM is a statistical sequential model which is able to use baysian 
approach to make such prediction without dictionary. In the framework of HMM model, 
a state refers to the correct letter, a observation refers to the observed letter, 
given a sequence of observations, our task is to get the most possible sequence of 
states. Our project use Viterbi Algorithms for the task. There is a very detailed description 
of first order as well as second order HMM in this file [HMM.ipynb](https://github.com/mogolola/Second_order_HMM_for_typos_correction/blob/master/HMM.ipynb)

 This model is somehow limited. For instance, it only handles substitution errors. A better model is 
 suggestted also in the file. I didn't implement it because we tend not to use single HMM model in industry. 
 The one google using is introduced in file. You can also see this paper [Casey Whitelaw and Ben Hutchinson and Grace Y Chung and Gerard Ellis, Google Inc. using the Web for Language Independent Spellchecking and Autocorrection](https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/36180.pdf)




