# ![Marvel Logo](https://www.regmovies.com/static/dam/jcr:5914096c-fc7c-4fda-ace5-f46c1744faa7/MARVEL-title_Small.jpg)


# Project 3: Web APIs & Classification


Marvel superhero movies have been connecting with audience for decades and we want to continue to faciliate the connection. Marvel Studios is planning to create new characters to get appear in the new series between 2021-2025 (5-year plan).

In order to create new characters with the qualities, values, characteristics that our audience can relate and connect to the most, our research team has carried out the following project to find out the best classfication predictive model to predict the category of a given statement on super powers.

#### Data source

Reddit is a network of communities based on people's interests. We believe our audience who has interest in superheroes or superpowers have shared a lot of thoughts on this popular platform. Hence, we have collected datasets from here.

The two subreddits that we have selected are:

1. shittysuperpowers
2. godtiersuperpowers

Both subreddits address in common certain root problems that the described superpowers wishes to tackle. T

1. shittysuperpowers:

    C-Tier super powers, less serious, something sort of useful, but not really useful; shittysuperpowers tackle themes or problems that are perceived as generally futile or too big to solve.

    E.g. You can throw a banana and it will return to you like a boomerang.


2. godtiersuperpowers:

    God-Tier super powers, positive, superior and intellectual powers; godtiersuperpowers tackle themes/problems that are perceived more hopefully with an optimism for an eventual positive outcome.

    E.g. You can undo any car accident with a push of a button.

#### Types of model

Three models are developed and evalulated:

1. LogisticRegression
2. K Nearest Neighbor
3. Naive Bayes

#### Model evaluation

After building a predictive classification model, we need to evaluate the performance of the model, that is how good the model is in predicting the outcome of new observations test data that haven't been used to train the model.

The used metrics and methods for assessing the performance of predictive classification models, include:

1. Classification accuracy, representing the proportion of correctly classified observations, out of 100%.


2. Confusion matrix, which is 2x2 table showing four parameters, including the number of true positives, true negatives, false negatives and false positives.


3. Sensitivity, Specificity and Precision, which are three major performance metrics describing a predictive classification model, out of 100%.

#### Goal

With this model, our team will be able to make predictions on subreddit posts which category the superpowers mentioned in the posts belongs to. More precisely, we want to find out what kind of super powers our potential audience would consider positive or amazing , and what are shitty or lame.

Based on this information, we wil be able to identify the positve and negative abilities, desires, emotions, values etc. and apply them on the design of our new movie series characters.

Since the new movie series is a 5-year plan, a reliable and accurate classfication predictive model is necessary. We will present our findings to our producers, directors or even actors for their decision making, on storylines and character development. Ultimately, Marvel Studios will be able to come up with more creative, innovative, inspiring superheroes with appealing super powers that audience likes. No matter to the primary stakeholders like filmmakers, or our secondary skateholders, which are our audience, this classification model will generate a lot of insights for our team.


##  Executive Summary

In the past few decades, Marvel Studios has been producing a series of superhero films, based on characters that appear in Marvel Comics publications. The mission statement for Marvel Studios is: A vision as far-reaching as our stories. “ Our mission to expand enables our legends like Thor and The X-Men to come to life in unexpected ways. And our mission is also to resonate with people today.

However, the Marvel Cinematic Universe (MCU) has had no shortage of critics. Certainly some have been disappointed in quality or storylines, character development or entertainment value, all of which are to be expected. Viewers and members of Hollywood alike debate the human authenticity of superhero films. It has been said by some that they’re “despicable”, silly and lacking conviction, others that they’re devoid of human emotion and experiences.

We want to produce Superhero movies that have values. They can bring hope and strength to those facing adversity, and a break from reality to everyone who steps foot into that theater or streams a movie from the comfort of their home.

Simply by searching what kind of super powers people are interested in isn't enough, we want to further understand and predict what category of a certain super power that audience consider it as. In order to classify the posts content and its words into one of the two classes (shittysuperpowers, godtiersuperpowers), a classfication model is needed.

We expect this model to help us create few new characters that contains those superpowers that audience consideres as god-tier, intellectual, positive, and superior. Hence, Marvel Studios will gain back reputation with good movie quality and signification.  

### Contents:
1. [Data Collection](#Data-Collection)
2. [Data Cleaning & EDA](#Data-Cleaning-&-EDA)
3. [Preprocessing & Modeling](#Preprocessing-&-Modeling)
4. [Conclusion & Recommendation](#Conclusion-&-Recommendation)



### Result

Parameters to Select Best Model:

1. Test acuracy Score: cvec_nb got the highest 0.670 out of 1.
2. Sensitivity: cvec_knn got the highest 0.804 out of 1.
3. Specificity: tvec_knn got the highest 0.697 out of 1.
4. Precision: cvec_nb got the highest 0.675 out of 1.

Overall, cvec_nb has the strongest score as it has the highest accuracy score and precision score.


## Conclusion & Recommendation

We believe applying a classfication predictive model into our decision making process is essential. A superhero character is the core of a movie, and the new movie series is a long term 5 year plan that is involved a huge amount of investment, no matter time or money. Hence, a reliable and accurate model is very important.

In this project, our research team has compared 3 models and evalued them with classficaiton metrics to decide which one is the best, which is **CountVectorizer + Naive Bayes**. Its accuracy score is 0.671 out of 1. Compare to baseline accuracy score 0.502, this model has shown an improved accuracy score. Moreover, we have also generated the best parameters for this model and it will be applied in the future use.

Marvel Studios strives to create innovative and inspiring superheroes with super powers that audience dreams of, as these super powers contain people's wishes, desires and hopes. For example, the top few words in both subreddits share few words, like time, control, change.

Hence directors or producers can consider a superhero who has the super power to stop time instantly or rewind or fastforward for the upcoming movie series. The dataset was collected in late September 2020, if we dive deeper, we can also analyze if these super powers are related external environments, for example, maybe due to Covid situation, people feel like they are running out of time and wish to own such a power to multitask in daily life. Depending on the circumstances and external factors, audience will have changing desires for super powers over time. Moreover, with the help of model, we can understand how the audience interprets a certain kind of super power if they see it as shitty or god tier super power. And film producers can decide what kind of super powers shouldn't be included in a movie.

We look forward to the insights that the model will provide our company and help us with the storyline, character development.

### Recommendations

No models are perfect. And below are some points that can be improved in the future to make this model even better:

1. N-Gram Range

    When preprocessing the data for modeling, I only removed stop words in the posts but didn't use N-Gram Range - it has the ability to capture n-word phrases. Since we are predicting based on text context, sometimes there are phrases that comprises of more than one single word, and using N-Gram Range can possibly help us prepare a better set of data for modeling and improve the accuracy.

2. A larger dataset is needed.

    We have collected only around 1000 posts from each subreddit for the modeling. The scale is pretty small to provide convincing result. Hence, with a bigger size of dataset, I believe the modeling can attain better scores.
