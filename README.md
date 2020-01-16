# ml-notes
notes for any dev who may be interested in learning machine learning basics

## table of contents:
[what is it?](#what-is-it)\
[why use it?](#why-use-it)\
[two types of learning...](#two-types-of-learning)\
[more about supervised learning](#lets-talk-about-supervised-learning-a-little-more)\
[classification example](#lets-take-a-look-at-a-classification-example)\
[regression example](#now-lets-look-at-a-simple-regression-example)\
[algorithms](#lets-look-at-a-few-machine-learning-algorithms)\
[decision tree](#decision-tree)\
[decision tree algorithm](#decision-tree-algorithm)\
[random forest](#random-forrest)\
[adaboost](#adaboost)\
[gboost](#gboost)\
[learning rate](#learning-rate)\
[gboost and random forest combined!](#gboost-and-randomforest-combined)\
[a great youtube series!](#a-great-youtube-series)


## what is it?
according to merriam-webster, machine learning is “the process by which a computer is able to improve its own performance by continuously incorporating new data into an existing statistical model.” ... basically, you create a "model" that takes in data, and based on that data, it will make future decisions.

... by the way, a **"model"** is essentially an algorithm that produces a probability in one form or another.

## why use it?
PREDICTION! we, as humans, have a hard time predicting the future; however, with machine learning, we can take a lot of the bias out of prediction in order to, hopefully, make it more accurate.

## two types of learning...
**supervised** and **unsupervised** learning. 

**supervised learning** is is a method of learning where the data given to a machine is labeled with the correct value, and the machine learns through comparing its predictions to the correct data.

**unsupervised learning** is a method of learning where the data given to a machine has no correct “answers,” and the machine attempts to make sense of the data. we essentially go to the machine and ask it to find patterns or trends in the data that we may not initially see.

## let's talk about supervised learning a little more
**classification** is where the machine will attempt to categorize the data based on specific attributes. this works well for categories (think female, male, etc.)

**regression** is where the machine will attempt to fit a given function to the given set of data (think a line best fit, quadratic equation best fit, etc.). this can work well for numerical (continuous) data. (2)

## let’s take a look at a classification example…
a good example of a machine learning classification problem is image recognition.
Consider a model that we want to recognize a cat in a given photograph. we would have thousands, even millions, of photographs. some of them contain a cat, and some of them don’t. 
when we feed the machine this data, the machine will inevitably mark some pictures as cats when they are not, and vice versa. however through this process, it picks up on details that distinguish the cat images from the ones without. 
after we are happy with the accuracy of our model, we can now use it on real images!

## now, let’s look at a simple regression example…
consider the case that we want to predict the price of a house based on specific attributes. let’s say we are given square footage and the number of rooms in the house. 
let’s create a ratio of square footage to number of rooms (ft^2/#rms). now we can plot the ratio as x, and the price of the house as y. 
say that we notice there seems to be a linear correlation with these plotted values. because of this, we decide to train the machine with a linear regression algorithm. the machine will now attempt to fit the line the best it can in order to best predict the prices and limit our **loss**.

## what is loss?
loss, in general terms, is the amount the predicted value deviates from the actual value.
for the most part, while training these models and creating these algorithms, our goal is to minimize loss. 


# let’s look at a few machine learning algorithms… 

## decision tree
before we learn about the decision tree algorithm, we need to learn about a decision tree. take the picture below as an example. this tree predicts the likelihood of a passenger’s survival on the titanic. at each feature (“is sex male,” “is age greater than 9.5 years,” “is the number of spouses and/or children the individual has greater than 2.5”) answer yes (move down & left) or no (move down & right) until you reach a prediction (died or survived) with the probability ( from 0-1).

![decision tree example](https://upload.wikimedia.org/wikipedia/commons/f/f3/CART_tree_titanic_survivors.png)\
Source: https://en.wikipedia.org/wiki/Decision_tree_learning


## decision tree algorithm
the algorithm will begin by taking all the data along with the features pertaining to that data and “split” the data on each feature in order to reduce the cost (which is basically how much the predicted data deviates from the actual data). it will continue to split on each subgroup recursively until all the features have been used. the tree can also be shortened by specifying the maximum number of features to be used or the maximum number of levels in the tree.

## random forrest
in the random forest algorithm, the computer will essentially create many unique decision trees, and based on the majority output of these trees, it will make a prediction (see right). the computer will create these “random trees” by randomly selecting different parts of the data set, and from that data set, randomly selecting a feature to split on (unlike the decision tree algorithm) in order to create a tree.

## adaboost
adaboost will work in a similar manner as the random forest algorithm (in most cases) with three big differences: the decision trees will be only a node a two leaves (a stump), it will take into account the errors other trees make, and each tree will not necessarily have the same voting power

## gboost
gboost works similar to adaboost in the same way it takes into account the previous tree’s mistakes in order to create the next tree; however, each tree will be scaled to have the same voting power, the user can define the number of leaves the tree will have, and the algorithm adjusts the “learning rate” based on the previous tree’s mistakes.

## learning rate
it basically controls how quickly the model adapts to the problem…also called the “step size.”

## gboost and randomforest combined!
this combination is powerful in the way that you can also define how many trees that will be created and the depth of the trees while also having the advantages of random forest.

## a great youtube series!
this is a great video series for some of the most important machine learning topics:
https://www.youtube.com/playlist?list=PLblh5JKOoLUICTaGLRoHQDuF_7q2GfuJF

**sources I used to create this overview:**\
https://www.youtube.com/playlist?list=PLblh5JKOoLUICTaGLRoHQDuF_7q2GfuJF
https://www.merriam-webster.com/dictionary/machine%20learning
https://medium.com/quick-code/regression-versus-classification-machine-learning-whats-the-difference-345c56dd15f7
https://machinelearningmastery.com/adam-optimization-algorithm-for-deep-learning/
https://towardsdatascience.com/decision-trees-in-machine-learning-641b9c4e8052
https://towardsdatascience.com/understanding-random-forest-58381e0602d2


