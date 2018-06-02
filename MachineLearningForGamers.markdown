## Machine Learning for Gamers: Dungeons Forecasts and Dragons Regressions
# by Guy Royse from Nexosis

# What is Machine Learning?
- Self-Learning algorithms that done by feeding datasets. "Computer Scientists discovered math and called it machine learning"
- Deep Learning is part of machine learning is part of artificial intelligence. There are some basic algorithms that can mimic what things do in artificial learning.
- Artificial intelligence is mimicking what humans can do such as image recognition, driving.
- Machine learning is around data analysis aspect of Artificial Intelligence. Lots of math around neural networks, math algorithms.
- Big Foot Sightings DB: http://www.bfro.net/GDB/ 

# How does it work?
- Gather data. Build a model. Make predictions from that model.
- Target: the thing you want to predict. 
- Features: Things that affect the thing we want to predict. 

# Gathering Data
- Encoding: converting non-numeric data to numeric data
- Imputation: replacing nulls with meaningful defaults
- One-Hot Encoding is turning text into numbers by defining an array of numbers that match that text
- Boolean Encoding

# Building a Model
- Pick out your algorithms. There are several.
- Set some of your data as training data and some data as test data. For example, take 80 percent to train and 20 percent to test with. You can also round-robin it with different buckets of test/train data so you can use all your data to do both. From that, you get a model.
- Then you run it, and it fails. 

## Finding a Good Model and Data Munging Errors
- target leakage: when you something you thought was a feature, but it is actually the target. For example, say you are targetting power, and you are using voltage and amperage as a feature. Voltage and amperage is power, so your data will be overfitted.
- Maybe you picked the wrong features or is missing some features you didn't account for.
- Maybe it's not enough data
- You are trying to find the trend of the data and understand its pattern as opposed to directly fitting because the model always knows what its looking at and can't deviate correctly when it finds a new thing.

## Making Predictions
Basically a prediction method looks like this.
```
let features = [f1, f2, f3]
let predicition = model.predict(features);
```

## Regression
- For example, predict how much gold a dragon has based upon its age, color, health, and the value of its treasure
- So you get a test data with these columns and randomly take test data
- Then you can ask, if I provide age, color, and health, then what is the hoard value the dragon keeps?

## Classification
- Classification is about predicting categories versus regression which is predicting a number. If you wanted to ask, depending on the hoard value, health, and age -- what is its color <-- that's a classification question.




