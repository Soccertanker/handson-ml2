# Chapter 1 Exercises

1. How would you define Machine Learning?

* A computer program is said to learn from experience E with respect to some task T and some performance measure P, if its performance on T, as measured by P, iimproves with experience E.
* Machine Learning is the field of study that gives computers the ability to learn without being explicitly programmed.

2. Can you name four types of problems where it shines?

* Problems for which existing solutions require a lot of fine-tuning or long lists of rules: one Machine Learning algorithm can often simplify code and perform better than the traditional approach.
** Spam filter: traditionally it may require a lot of rules to sort out which emails are spam.
** Machine Learning gives the computer classified training sets when users flag emails as spam, allowing the computer to make rules and find which rules are most important to classify emails. CPU can fine-tune much easier than humans can.
* Complex problems for which using a traditional approach yields no good solution: the best Machine Learning techniques can perhaps find a solution.
** Speech recognition: traditional approach has no good solution to decipher words from so many different voices, accents, and contexts.
** Machine Learning could find patterns that are too complex for humans to model in a traditional algorithm.
* Fluctuating environments: a Machine Learning system can adapt to new data.
** Spam filter: companies often change how their spam looks over time, to avoid spam filters.
** Machine Learning models can incrementally train on new data and adapt to be able to detect new spam emails.
* Getting insights about complex problems and large amounts of data.
** Humans can inspect Machine Learning algorithms to see what they have learned.
** This can lead to a better understanding of data. This is called *data mining*.

3. What is a labeled training set?

* A labeled training set is the training set fed to a *supervised learning* algorithm, which includes the desired solutions, called *labels*.

4. What are the two most common supervised tasks?

* Classification and regression.
** Classification is used to label new data with their *class*.
** Regression predicts a target numberic value given a set of features called predictors. 

5. Can you name four common unsupervised tasks?

* Clustering, anomaly detection and novelty detection, visualization and dimensionality reduction, association rule learning.
** Clustering divides data into groups of similar data. Maybe Google uses search history to divide people into different groups to give the same advertisements to the people in the same groups.
** Dimensionality reduction merges correlated features into one. For example, if we measure height and weight of professional runners, who all have the same body shape, these two features give basically the same information. Taller runners will weigh more. Reducing these two features into one feature would simplify the dataset.
** Anomaly detection is self-explanatory. An example is when credit card companies call you saying your credit card was used in another country. They know the locations where your credit card is usually used, so their Machine Learning algorithms can detect anomalies of your credit card being used somewhere unexpected.
** Association rule learning finds interesting relations between attributes. It may  learn that people who buy tortilla chips also tend to buy salsa, so a store manager may want to place chips and salsa near each other in the store (or not; make the fat people walk further).

6. What type of Machine Learning algorithm would you use to allow a robot to walk in various unknown terrains?

* Batch learning: because the terrains are unknown, we might not be able to make a good training set for them. And the robot may not be able to store a ton of memory. The robot could use new bits of data to incrementally learn about the terrains as it walks on them.

7. What type of algorithm would you use to segment your customers into multiple groups?

8. Would you fram the problem of spam detection as a supervised learning problem or an unsupervised learning problem?

9. What is an online learning system?

10. What is out-of-core learning?

11. What type of learning algorithm relies on a similarity measure to make predictions?

12. What is the difference between a model parameter and a learning algorithm hyperparameter?