# SpotLight: Detecting Anomalies in Streaming Graphs

[Download link](https://dl.acm.org/doi/10.1145/3219819.3220040)


## New points of view

I saw detecting disappearing items in the graph for the first time and not repeated in the articles


This article has a random uniform sketching method so that it extracts items from graph

And after that it will help finding out what is happening with smaller portion of data being added not the whole

Algorithms that use precision & recall: 

+ Edge weight
+ Spot light
+ STA


Metrics like precision@K and recall@K


## Ideas and relation to my work

+ Detect changes in reverse direction values that has been reduced since the last epoch
+ Detect items that has incoming and outgoing degree
+ Focus on speed and parallel running algorithms