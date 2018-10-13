# Sampling Methods

In the age of Big Data, we are tempted to deal with bias by collecting more data. After all, we know that a census will give us perfect estimates; shouldn't a very large sample give almost perfect estimates regardless of the sampling technique?

## Probability Sampling

Unlike convenience sampling, probability sampling allows us to assign a precise probability to the event that we draw a particular sample.

### Simple Random Sample (SRS):

Suppose we have a population of 6 individuals. We've given each individual a different letter from A−F.
To take an simple random sample of size 2 from this population, we can write each letter A−F on a single index card, place all the cards into a hat, mix the cards well, and draw 2 cards without looking. That is, a SRS is sampling uniformly at random without replacement.

Here are all possible samples of size 2: AB, AC, AD, AE, AF, BC, BD, BE, BF, CD, CE, CF, DE, DF, EF.

There are 15 possible samples of size 2 from our population of 6. Another way to count the number of possible samples is:
```
(6C2) = 6!/ 2!4!=15
```

Since in a SRS we sample uniformly at random, each of these 15 samples are equally likely to be chosen: 
```
P(AB)= P(CD)= …= P(DF)= 1/15
```

We can also use this chance mechanism to answer other questions about the composition of the sample. For example:
```
P(A in sample)=5/15=1/3
```
Since 5 out of 15 of the possible samples listed above contain A.

 ###Two alternative methods of probability sampling: cluster sampling and stratified sampling

### Cluster sampling:
In cluster sampling, we divide the population into clusters. Then, we use SRS to select clusters at random instead of individuals.

As an example, suppose we take our population of 6
individuals and we pair each of them up: (A,B)(C,D)(E,F) to form 3 clusters of 2 individuals. Then, we use SRS to select one cluster to produce a sample of size 2.

### Stratified sampling
