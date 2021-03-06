# Chapter 1 Exercises

1. How would you define Machine Learning?

* A computer program is said to learn from experience E with respect to some task T and some performance measure P, if its performance on T, as measured by P, iimproves with experience E.
* Machine Learning is the field of study that gives computers the ability to learn without being explicitly programmed.

2. Can you name four types of problems where it shines?

* Problems for which existing solutions require a lot of fine-tuning or long lists of rules: one Machine Learning algorithm can often simplify code and perform better than the traditional approach.
    * Spam filter: traditionally it may require a lot of rules to sort out which emails are spam.
    * Machine Learning gives the computer classified training sets when users flag emails as spam, allowing the computer to make rules and find which rules are most important to classify emails. CPU can fine-tune much easier than humans can.
* Complex problems for which using a traditional approach yields no good solution: the best Machine Learning techniques can perhaps find a solution.
    * Speech recognition: traditional approach has no good solution to decipher words from so many different voices, accents, and contexts.
    * Machine Learning could find patterns that are too complex for humans to model in a traditional algorithm.
* Fluctuating environments: a Machine Learning system can adapt to new data.
    * Spam filter: companies often change how their spam looks over time, to avoid spam filters.
    * Machine Learning models can incrementally train on new data and adapt to be able to detect new spam emails.
* Getting insights about complex problems and large amounts of data.
    * Humans can inspect Machine Learning algorithms to see what they have learned.
    * This can lead to a better understanding of data. This is called *data mining*.

3. What is a labeled training set?

* A labeled training set is the training set fed to a *supervised learning* algorithm, which includes the desired solutions, called *labels*.

4. What are the two most common supervised tasks?

* Classification and regression.
    * Classification is used to label new data with their *class*.
    * Regression predicts a target numberic value given a set of features called predictors. 

5. Can you name four common unsupervised tasks?

* Clustering, anomaly detection and novelty detection, visualization and dimensionality reduction, association rule learning.
    * Clustering divides data into groups of similar data. Maybe Google uses search history to divide people into different groups to give the same advertisements to the people in the same groups.
    * Dimensionality reduction merges correlated features into one. For example, if we measure height and weight of professional runners, who all have the same body shape, these two features give basically the same information. Taller runners will weigh more. Reducing these two features into one feature would simplify the dataset.
    * Anomaly detection is self-explanatory. An example is when credit card companies call you saying your credit card was used in another country. They know the locations where your credit card is usually used, so their Machine Learning algorithms can detect anomalies of your credit card being used somewhere unexpected.
    * Association rule learning finds interesting relations between attributes. It may  learn that people who buy tortilla chips also tend to buy salsa, so a store manager may want to place chips and salsa near each other in the store (or not; make the fat people walk further).

6. What type of Machine Learning algorithm would you use to allow a robot to walk in various unknown terrains?

* I would use a supervised learning algorithm to teach a robot to walk in unknown terrains. The algorithm could use data that it captures from the unknown terrains and classify the terrain as the most similar terrain that it knows about.
* Online learning: because the terrains are unknown, we might not be able to make a good training set for them. And the robot may not be able to store a ton of memory. The robot could use new bits of data to incrementally learn about the terrains as it walks on them.

7. What type of algorithm would you use to segment your customers into multiple groups?

* Clustering algorithms can group customers into multiple groups based on customer data.

8. Would you frame the problem of spam detection as a supervised learning problem or an unsupervised learning problem?

* I would frame spam detection as a supervised learning problem. A supervised learning problem would work well because the machine can learn what a spam email looks like by analyzing a training set with data labeled as spam or ham.
* If we used an unsupervised learning algorithm like clustering, the algorithm may or may not group spam emails into one cluster. But spam emails can be so varied, so a clustering algorithm or other unsupervised algorithm might not have great results.
    * On the flip-side, maybe associate rule learning could make relations about different features that ham emails have in common and that spam emails have in common. Maybe this could inform humans about what features spam emails have.

9. What is an online learning system?

* In online learning, you train the system incrementally by feeding it data instances sequentially, either individually or in small groups called mini-batches.
* Each learning step is fast and cheap, so the system can learn about new data on the fly, as it arrives.
* It doesn't necessarily mean the system is *online*. Often, the system is offline, not on the live system. *Online* learning is synonymous with *incremental* learning.

10. What is out-of-core learning?

* Out-of-core learning is usually done offline.

11. What type of learning algorithm relies on a similarity measure to make predictions?

* Instance-based learning can use a measure of similarity between data to generalize known example data to new data.

12. What is the difference between a model parameter and a learning algorithm hyperparameter?

* A model parameter is a degree of freedom for an algorithm's model. If a model has two degrees of freedom, it can adjust the height and slope of a model, and the model will be linear.
* A learning algorithm hyperparameter controls the amount of regularization to apply during learning. It is not affected by the learning algorithm, but is a parameter that the learning algorithm must adjust its model to fit.
* The difference is that model parameters are made by the learning algorithm, when the algorithm is fitting a model to the data, whereas the learning algorithm hyperparameter is an algorithm parameter that affects how the model is made, and how well the model fits the data.

13. What do model-based learning algorithms search for? What is the most common strategy they use to succeed? How do they make predictions?

* Model-based learning seeks to generalize from a set of examples to build a model of these examples and then use that model to make predictions (page 18).
* The most common strategy they use is to find model parameters that fit the data, and test how well those model parameters work to predict features of new data (page 20)

14. Can you name four of the main challenges in Machine Learning?

* Yes.
    1. Insufficient quantity of training data: machine learning requires a lot of data to learn well. Toddlers can look at one apple and identify any fruit as being an apple or not. But machine learning algorithms can't do this; they need to look at tons of examples of apples and other fruits that are not apples (page 23).
    2. Nonrepresentative training data: a machine learnign algorithm that is trained on nonrepresentative training data will learn improperly and not be as useful on non-training data (page 25).
    3. Irrelevant features: the system will only be capable of learning if the training data contains enough relevant features and not too many irrelevant ones. Feature engineering uses feature selection to select the most relevant features, feature extraction to combine features to produce a more useful one, and create new features by gathering new data (page 27).
    4. Overfitting the training data: a model may try too hard to fit the training data. If the machine learning algorithm overgeneralizes the training data, it may think all new data will follow this model. A model may perform better on new data if it can generalize better (page 27).

15. If your model performs great on the training data but generalizes poorly to new instances, what is happening? Can you name three possible solutions?

* The model is overfitting. It is too complex relative to the amount and noisiness of the training data (pages 27-28). The solutions can be:
    1. Simplify the model by selecting one with fewer parameters, by reducing the number of attributes in the training data, or by constraining the model.
    2. Gather more training data.
    3. Reduce the noise in the training data.

16. What is a test set, and why would you want to use it?

* The test set is a set of data that a model is tested with. Evaluating a model on the test set gives an estimate of the generalization error, which is the error rate on new data (page 30).

17. What is the purpose of a validation set?

* The validation set is a portion of the training set that is held out from training, and used to evaluate several candidate models (page 31).

18. What is the train-dev set, when do you need it, and how do you use it?

* The validation and testing data should be as representative of new data as possible. Thus the training data may not be as representative, and is vulnerable to data mismatch. For example, maybe training data is pictures taken from the web, but validation / testing data is pictures taken by phones, which is more representative of the data that the algorithm will eventually be fed (page 32).
* The train-dev set is useful to troubleshoot a bad model, with potential data mismatch between the training data and the validation / testing data. The train-dev set is a portion of the training set that is held out for validation.
    * If the candidate model performs well on the train-dev set, then it is not overfitting the training set. This means any problems are likely because of a data mismatch between the training data and the validation / test data.

19. What can go wrong if you tune hyperparameters using the test set?

* Tuning hyperparameters using a test set can potentially cause a model to be overfit for the test set, and not generalize well with other test sets (page 31).
