# master-docs
Master documentations and download links

## Datasets

+ DARPA => [Reference](./articles/0001-Sketch-Based%20Anomaly%20Detection%20in%20Streaming%20Graphs/)
+ ISCX-IDS2012 => [Reference](./articles/0001-Sketch-Based%20Anomaly%20Detection%20in%20Streaming%20Graphs/)
+ CIC-IDS2018 => [Reference](./articles/0001-Sketch-Based%20Anomaly%20Detection%20in%20Streaming%20Graphs/)
+ CIC-DDoS2019 => [Reference](./articles/0001-Sketch-Based%20Anomaly%20Detection%20in%20Streaming%20Graphs/)
+ Amazaon => [Reference](./articles/0005-From%20amateurs%20to%20connoisseurs%20modeling%20the%20evolution%20of%20user%20expertise%20through%20online%20reviews/)
+ YelpChi => [Reference](https://dl.acm.org/doi/abs/10.1145/2783258.2783370) Not very good not very good accessible
+ TwitterSecurity dataset => [Download link](https://odds.cs.stonybrook.edu/twittersecurity-dataset/)

+ Elliptic(BitCoin) => [Reference](./articles/0003-DGraph%20A%20Large-Scale%20Financial%20Dataset%20for%20Graph%20Anomaly%20Detection/),
[Kaggle](https://www.kaggle.com/datasets/ellipticco/elliptic-data-set/),[Reference](https://arxiv.org/abs/1908.02591)

+ Epinions => [Reference](https://dl.acm.org/doi/abs/10.1145/3159652.3159729), [Download link](https://snap.stanford.edu/data/soc-Epinions1.html)

+ DBLP (Citation Network Dataset): [Download link](https://paperswithcode.com/dataset/dblp) This dataset is new and has been used recently. My challenge is how to find anomaly labels
Many datasets in [this link](https://www.aminer.cn/citation) and even big sizes


## Good links
[Stanford Large Network Dataset Collection](http://snap.stanford.edu/data/)


## Ideas to generate dataset

1. Transform Node Labels to Edge Labels:


If you have a dataset where nodes are labeled as anomalous or legitimate, you can potentially infer the labels for edges by analyzing the relationships between the nodes connected by those edges.
Approach:
+ Legitimate-Legitimate Edge: If both nodes are labeled as legitimate, it is reasonable to label the connecting edge as legitimate.
+ Anomalous-Anomalous Edge: If both nodes are labeled as anomalous, the edge between them is likely anomalous.
+ Mixed Edge: If one node is legitimate and the other is anomalous, this edge might also be considered anomalous, as the connection may indicate suspicious behavior (e.g., legitimate users interacting with malicious entities).


Assumptions: You would be making the assumption that the anomalousness of an edge is somehow related to the anomalousness of the nodes it connects, which is reasonable in many applications (e.g., cybersecurity, fraud detection).

After that I can run existing algorithms on newly generated dataset and after that evaluate the work

