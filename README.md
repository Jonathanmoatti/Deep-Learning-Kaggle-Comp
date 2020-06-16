# Deep-Learning-Kaggle-Comp
This is a project from my PhD level Deep Learning class supervised by Jian Tang at HEC Montreal

This is an in class kaggle competition on which i finished 5th/98.

The task at hand was a title classification. The datasets we were given consisted of text titles, and text references associated to said texts. We then needed to correctly classify these texts amongst 5 classes in total.

I tested several different models in this competition : 

For Deep Learning models i tested :
- Bi-directional LSTM with Glove 64B as embedding.
- CNN with FastText embeddings.
- GRU with BERT (bert-base-uncased)
Best deep learning single model was obtained with CNN with FastText embeddings.

For Machine Learning models i tested : 
- SVM with TF-IDF, tuned with bayesian optimisation on the pipeline (applied Bayesian Optimisation to both TF-IDF vectorizer and SVM)
- MultinomialNB with TF-IDF, tuned with bayesian optimisation on the pipeline
- Logistic Regression with TF-IDF, tuned with bayesian optimisation on the pipeline
- LightGBM with TF-IDF, tuned with bayesian optimisation on the pipeline
- ExtraTrees with TF-IDF, tuned with bayesian optimisation on the pipeline
- XGboost with TF-IDF, tuned with bayesian optimisation on the pipeline
- RandomForest with TF-IDF, tuned with bayesian optimisation on the pipeline
Best single machine learning model was obtained with SVM.

Best overall model was obtained by combining three of my optimized models with very different underlying algorithms: SVM, MultinomialNB and LightGBM, and putting them in a VotingClassifier.
