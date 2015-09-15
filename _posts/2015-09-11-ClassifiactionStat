---
layout: post
title: Stastical Evaluation of Classifiers
---


Imagine that you're trying to classify politicians into two groups: 
those who are honest, and those who are not. I'll give you a list of 100 people, half of which are honest, and you'll give me a list of all the honest ones, but being careful not to accidentally include anyone who is not.

Having high precision means that when you do say that someone is honest, you're usually right about it. This is about how many politicians in your list are actually honest, out of all the ones that you've added to the list.

Having high recall means that you can identify most of the honest politicians out there. This is about how many honest politicians you've added to your list, out of all the ones that exist.

Note that these are not the same. You could add a single honest politician to the list. You would then have very high precision, since the only person that you've listed is actually honest; but you would also have very low recall: there are 50 honest politicians out there but you've only mentioned one.

Ideally, you'd want to list all honest politicians that exist while being careful to not accidentally include some who are not. If you could do that, then you'd have both high precision and high recall. 

When measuring how well you're doing, it's often useful to have a single number to describe your performance. We could define that number to be, for instance, the mean of your precision and your recall. This is exactly what the F1-score is. 

The only reason why we use the harmonic mean is because we're taking the average of ratios (percentages), and in that case the harmonic mean is more appropriate than the arithmetic mean.

-----

You are trying to determine how well your system performs. The most obvious way to see this is how accurate it is; of your testing example, what percentage did you classify correctly? For example, lets say we have 1000 people, and you are predicting if they will like a tv show or not. 990 of them won't, and 10 will. If you simple say nobody likes it, your accuracy is very high, you were 99% accurate. However, you identified 0% of the people who would have liked the show, which is not a very good performance.
So, we instead measure 2 values, precision and recall
precision is how accurate you are about saying that somebody will like your show. if I said that 8 people will like the show, and 6 of them do, then my accuracy is 75%
recall is how good you are at identifying the ones that like it. There are 10 people who like the show, and I was able to identify 6 of them as people who would like it, I have a 60% recall.

Both of these are useful and needed. If I say nobody likes the show, I have a 0% recall, which is bad. if I say everyone likes it, I have a 100% recall, but my accurate is 1%. As I try out different strategies, I need a way to figure out is one pair of numbers is better than another. The simple way would be to average them.  
However, this create some undesirable results. Take my "everyone likes it" metric. 100% recall and 1% precision is an average of 50%. However, I am doing awful on this task, nowhere near a 50% performance. If I picked out 10 people to like the show, and 5 of them like it, my precision is 50%. I also identified 5 of the 10 people who liked the show, so my recall is 50%. This is a much better performance than the "everyone likes it" metric, and it seems like it actually is getting a 50% score. So, its better to have the two scores be close together than far apart. But obviously higher numbers are better. 

The harmonic mean is like the average, but it also takes into account how similar the two values are. 

Say I have a precision of 80% and a recall of 15%. if I could modify my system so the precision is 70% but the recall is 20%, it is performing better.
The first case has  F measure of 25.3%. The second is 31%. Even though your average goes down between the two, it is more important to increase your recall so the precision drop is worth it. The F-score allows you to judge just how much of a tradeoff is worthwhile. If I made my system have a 30% precision for a 20% recall, my F-measure would be 24%, and the tradeoff wouldn't be worth it.
