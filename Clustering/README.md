### Assignment

### Clustering

Step 1: Randomly pick K points to place K centroids
Step 2: Assign all the data points to the centroids by distance. The closest centroid to a point is the one it is assigned to.
Step 3: Average all the points belonging to each centroid to find the middle of those clusters (center of mass). Place the corresponding centroids into that position.
Step 4: Reassign every point once again to the closest centroid.
Step 5: Repeat steps 3-4 until no point changes which centroid it belongs to.


#### Data
Let's start by discussing the type of data we use when we work with a hidden markov model.

In the previous sections we worked with large datasets of 100's of different entries. For a markov model we are only interested in probability distributions that have to do with states.

We can find these probabilities from large datasets or may already have these values. We'll run through an example in a second that should clear some things up, but let's discuss the components of a markov model.

States: In each markov model we have a finite set of states. These states could be something like "warm" and "cold" or "high" and "low" or even "red", "green" and "blue". These states are "hidden" within the model, which means we do not direcly observe them.

Observations: Each state has a particular outcome or observation associated with it based on a probability distribution. An example of this is the following: On a hot day Tim has a 80% chance of being happy and a 20% chance of being sad.

Transitions: Each state will have a probability defining the likelyhood of transitioning to a different state. An example is the following: a cold day has a 30% chance of being followed by a hot day and a 70% chance of being follwed by another cold day.

To create a hidden markov model we need.

States
Observation Distribution
Transition Distribution
For our purpose we will assume we already have this information available as we attempt to predict the weather on a given day.

## standard deviation
We will model a simple weather system and try to predict the temperature on each day given the following information.

Cold days are encoded by a 0 and hot days are encoded by a 1.
The first day in our sequence has an 80% chance of being cold.
A cold day has a 30% chance of being followed by a hot day.
A hot day has a 20% chance of being followed by a cold day.
On each day the temperature is normally distributed with mean and standard deviation 0 and 5 on a cold day and mean and standard deviation 15 and 10 on a hot day.
If you're unfamiliar with standard deviation it can be put simply as the range of expected values.

In this example, on a hot day the average temperature is 15 and ranges from 5 to 25.

#### Conclusion
So that's it for the core learning algorithms in TensorFlow. Hopefully you've learned about a few interesting tools that are easy to use! To practice I'd encourage you to try out some of these algorithms on different datasets.