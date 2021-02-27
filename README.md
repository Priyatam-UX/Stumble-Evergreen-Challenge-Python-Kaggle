Stumble-Evergreen-Challenge-Python-Kaggle
=====================

My solution in Python for the kaggle problem StumbleUpon Evergreen Classification Challenge


Approach
---------
The problem dealt with webpage classification, the performace was dominated by the features of webpage text, as it gave max relevant features.
We had to use NLP methods - owing to the brilliance of sklearn package, we could use the TFID techniques to vectorize our inputs. 
Since a problem of NLP at its best, The TFID approach was tuned with different parameters like different n-grams,norm, df, token patterns, customized tokenizers.
We also used Latent Semantic Analysis (Truncated SVM in this case), as we got amazing results when we reduced the components correctly (BUT, This brings a crazy Variance in our model!)
Quite a lot of classifiers were tried but we sticked with Logsistic Regression and moreoever used an ensemble of logistic regression models (the data was divided using k-fold cross validation.
GridSearch was used to search for the best matching parameters as well.
Surprisingly, SVMs didnt work in this one(all kernels were tried in hope) to that extent and moreover it took plenty of time to train.

Files
-------
stumble.py - The core file containing the implementation.

stumble-51.csv - This was one of the setting when I got the best rank of 61. This is the submission file prepared from code.

kaggle-51.jpg - The screenshot showing the same (total 625 teams), But crazy variance has slightly different results each time (LSA!)

Libraries used (Dependencies)
----------------
numpy (For arrays mostly), 
pandas ,
sklearn (scikit-learn),
nltk (for stemmers) 
