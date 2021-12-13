# UVA DS6040: Final Project
Modeling Uncertainty for Spam

Team Members: Anahita Sharma (ahs3zq) and Elizabeth Lee (ewl3dv)

In this project, we used the UCI Machine Learning Repository Dataset for Spam emails. The dataset can be found here: https://archive.ics.uci.edu/ml/datasets/spambase. 

We cleaned the dataset, and used 49 variables from the original dataset. 48 of these features are the word_freq_WORD columns while the remaining column identified the class attribute of type spam {spam, ham}. 

- 48 continuous real [0,100] attributes of type word_freq_WORD = percentage of words in the e-mail that match WORD,

i.e. 100 * (number of times the WORD appears in the e-mail) / total number of words in e-mail.  A "word" in this case is any string of alphanumeric characters bounded by non-alphanumeric characters or end-of-string.


- 1 nominal {0,1} class attribute of type spam = denotes whether the e-mail was considered spam (1) or not (0), 

i.e. unsolicited commercial e-mail.  

We cleaned the 48 word_freq_WORD features into a binary index that marked spam as {1} and ham as {0}. If a word has a frequency above 0, they were indexed as spam {1}.

- For more information, see file 'spambase.DOCUMENTATION' at the UCI Machine Learning Repository: <http://www.ics.uci.edu/~mlearn/MLRepository.html>

To run our notebook the packages listed at the top of the notebook need to be installed. Some packages include but are not limited to pandas, numpy, matplotlib, seaborn, Pymc3, and arvis. 

Project goal: Beyond arriving at point estimates for the posterior probabilities of classifying an email as spam given a the parameters (words), the goal of this project is to map the uncertainty of these estimates. 
