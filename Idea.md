# Ideas

## My own ideas

+ combine sketch based anomaly detection with MIDAS
+ Threshold finding is an important task
+ analyze other edge stream data structures
+ make more general cms data structure to make result better
+ Use z-score to improve the scoring that can be compared with single value in different datasets

## Reference ideas

### Literature Review: Edge Anomaly Detection

Edge anomaly detection is a significant subfield of graph-based anomaly detection. It focuses on identifying unusual or unexpected relationships (edges) between nodes in a graph, such as in social networks, communication patterns, or transaction networks. Below are several methods used to detect edge anomalies, along with their descriptions, advantages, limitations, and some datasets commonly used for these tasks.

---

#### 1. **Rule-based Edge Anomaly Detection**

**How it Works:**  
Rule-based methods use predefined rules or heuristics to flag anomalous edges. These rules are often based on graph metrics such as node degree, edge weight, or the structural properties of the graph. Anomalous edges are those that violate these rules, such as edges that connect nodes with a significantly different degree or edges that break expected patterns of connectivity (e.g., a person with no mutual friends in a social network suddenly has many connections to others).

**Pros:**
- Simple and interpretable.
- Works well in well-structured graphs where domain knowledge is available.
  
**Cons:**
- Cannot adapt to complex patterns of anomalies.
- High false-positive rate in dynamic or less-structured graphs.

**Datasets:**
- **Enron Email Dataset:** Commonly used for rule-based anomaly detection, particularly for detecting unusual communication patterns between employees.
- **DBLP (for co-authorship networks)**

---

#### 2. **Statistical Methods**

**How it Works:**  
Statistical methods rely on modeling the normal behavior of edges using probability distributions. Any edge that deviates significantly from the expected distribution is flagged as an anomaly. Techniques like hypothesis testing, Gaussian mixture models, and others can be employed to estimate the likelihood of an edge being normal or abnormal.

**Pros:**
- Offers a solid foundation for analyzing well-distributed data.
- Can provide confidence intervals for anomalies.

**Cons:**
- Struggles with high-dimensional graphs or when the data distribution is unknown.
- Sensitive to model assumptions (normality, independence).

**Datasets:**
- **Citeseer Graph Dataset**
- **Facebook Social Network Dataset**

---

#### 3. **Machine Learning-based Approaches**

**How it Works:**  
Machine learning methods, including supervised, unsupervised, and semi-supervised learning, have been widely used for edge anomaly detection. Supervised learning techniques (e.g., SVM, Random Forest) require labeled examples of normal and anomalous edges. In contrast, unsupervised methods like clustering or autoencoders detect anomalies by learning representations of the graph and flagging unusual edges.

**Pros:**
- Scalable to large graphs.
- Can automatically learn complex patterns without manual rule crafting.
  
**Cons:**
- Supervised methods require labeled data, which may not always be available.
- Can be computationally expensive.
  
**Datasets:**
- **Cora Dataset (citation graph)**
- **Reddit Hyperlink Network**

---

#### 4. **Deep Learning (Graph Neural Networks - GNNs)**

**How it Works:**  
Deep learning techniques, particularly GNNs, are highly effective for capturing structural information in graph data. A GNN is trained to embed graph nodes into a vector space, preserving their relationships. Edge anomalies are detected by evaluating whether the edge is expected based on the learned embeddings. Variants like Graph Convolutional Networks (GCNs) and Graph Attention Networks (GATs) can also be used.

**Pros:**
- Handles complex, high-dimensional graphs.
- Learns rich representations without explicit feature engineering.

**Cons:**
- Requires large amounts of training data.
- Computationally intensive, requiring GPUs for efficient training.

**Datasets:**
- **OGBN-Arxiv Dataset (citation network)**
- **Twitch Social Network**

---

#### 5. **Spectral Methods**

**How it Works:**  
Spectral methods analyze the eigenvalues and eigenvectors of the graph’s adjacency matrix or Laplacian matrix to capture the overall structure of the graph. Anomalous edges are identified by studying deviations in the spectral space, where typical edges cluster in specific regions, and anomalies often reside outside these clusters.

**Pros:**
- Effective in identifying global structure-based anomalies.
- Theoretical guarantees under certain conditions (e.g., spectral clustering).

**Cons:**
- Less effective in very large or dynamic graphs.
- Sensitive to noise in the graph structure.

**Datasets:**
- **Internet Autonomous Systems Network**
- **Bitcoin Transaction Network**

---

#### 6. **Temporal Edge Anomaly Detection**

**How it Works:**  
Many real-world graphs are dynamic, meaning that the edges (connections between nodes) change over time. Temporal anomaly detection focuses on finding anomalous edges in dynamic graphs, by tracking the evolution of edges over time and flagging connections that change in unexpected ways, such as sudden spikes in activity or unexpected disappearance of edges.

**Pros:**
- Suitable for real-time applications where the graph is evolving (e.g., fraud detection, network monitoring).
  
**Cons:**
- Computationally demanding as it requires continuous monitoring of the graph.
  
**Datasets:**
- **DARPA Intrusion Detection Dataset (network activity)**
- **Stack Overflow Temporal Data (Q&A patterns over time)**

---

### Real-World Use Cases for Edge Anomaly Detection

1. **Fraud Detection in Financial Networks**
   - **Use Case:** Banks use edge anomaly detection to identify fraudulent transactions in financial transaction networks by finding unusual patterns in how money flows between accounts.
   - **Datasets:** **Elliptic Dataset**, **Bitcoin OTC Trust Weighted Signed Network**

2. **Social Media Fake Account Detection**
   - **Use Case:** Social platforms like Twitter or Facebook use edge anomaly detection to find fake accounts or botnets by analyzing unusual patterns in social connections or message exchanges.
   - **Datasets:** **Twitter Bot Detection Dataset**, **Facebook Page-Page Network**

3. **Telecommunication Network Monitoring**
   - **Use Case:** Telecom companies use edge anomaly detection to monitor their communication networks for abnormal traffic patterns that could indicate attacks or failures.
   - **Datasets:** **Telecom Italia SMS Network**, **DARPA Intrusion Detection Dataset**

4. **Cybersecurity in Computer Networks**
   - **Use Case:** Edge anomalies help detect intrusions, data exfiltration, or other network threats by finding unusual connections between computers, servers, or other network devices.
   - **Datasets:** **NSL-KDD Dataset**, **CICIDS2017 (network traffic data)**

5. **Recommendation Systems in E-commerce**
   - **Use Case:** E-commerce platforms like Amazon use edge anomaly detection to spot fake reviews or unusual purchase patterns by examining the graph of user-product interactions.
   - **Datasets:** **Amazon Product Co-purchasing Network**, **Yelp Dataset Challenge**

---

Each method and use case is designed to fit different scenarios based on the nature of the graph and the type of anomalies expected. Depending on the dataset or problem domain, you can choose a method that balances accuracy, scalability, and interpretability.

My idea to continue is that I use amazon dataset. so that I can understand the dataset well.