## 🧭 4-Layer Thesis Hierarchy: Threshold Detection for Anomaly Detection in Streaming Graphs (DDoS Domain)

---

### **Layer 1: Conceptual Foundations (Problem & Scope)**

1. **Introduction**

   * Background on anomaly detection in network security.
   * Emergence of streaming graphs in real-time network monitoring.
   * The challenge of thresholding in DDoS contexts.
   * Thesis problem statement.
   * Research objectives and contributions.

2. **Problem Domain**

   * Overview of DDoS attacks and graph-based detection.
   * Characteristics of streaming graphs in cybersecurity.
   * Formal definition of anomaly detection in graph streams.

3. **Research Challenges**

   * Threshold calibration in evolving data.
   * Sensitivity to concept drift and non-stationarity.
   * Performance trade-offs (accuracy vs memory/time).

---

### **Layer 2: Taxonomy and Landscape**

4. **Streaming Graphs: Models and Representations**

   * Dynamic graph modeling (edge/vertex stream, time-evolving graphs).
   * Memory-efficient representations (adjacency sketching, windowing).

5. **Anomaly Detection Techniques in Graph Streams**

   * Structural anomaly detection (e.g., degree deviation, centrality shifts).
   * Statistical profiling (e.g., local vs global metrics).
   * Temporal pattern deviation.

6. **Thresholding in Anomaly Detection**

   * Fixed thresholds: Pros/cons.
   * Adaptive thresholds: EWMA, CUSUM, etc.
   * Hybrid thresholding methods.
   * Literature review of thresholding in streaming models.

---

### **Layer 3: Methodology (Your Framework)**

7. **System Overview**

   * Input: Graph stream with time-stamped edges/nodes.
   * Real-time processing constraints.
   * Output: Anomaly label or score based on threshold.

8. **Statistical Models for Thresholding**

   * EWMA, z-score, IQR-based dynamic ranges.
   * Baseline scoring methods for streaming graphs.
   * Concept of score distribution evolution.

9. **Proposed Technique**

   * Design of hybrid/mixed thresholding pipeline.
   * Justification for chosen statistical components.
   * Real-time blending/selection mechanism.
   * Efficiency & complexity constraints.

---

### **Layer 4: Evaluation and Discussion**

10. **Experimental Setup**

* Dataset description (synthetic and/or real DDoS datasets).
* Metrics: Detection rate, false positive rate, latency, memory use.
* Tools and frameworks used.

11. **Results and Analysis**

* Comparative study with individual vs hybrid thresholding methods.
* Analysis under different attack intensities and graph dynamics.
* Trade-offs between responsiveness and stability.

12. **Discussion**

* Strengths and limitations.
* Scalability.
* Sensitivity to parameter choices (e.g., decay rate, window size).

13. **Conclusion and Future Work**

* Summary of findings.
* Potential for extension to other domains (e.g., fraud, sensor networks).
* Ideas for adaptive/self-tuning threshold models.

---

### Optional Layer 5 (Appendices / Extensions)

* A. Mathematical proofs (if applicable)
* B. Pseudocode or architecture diagrams
* C. Extended dataset details or anomaly case studies