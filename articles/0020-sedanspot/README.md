# SedanSpot: Detecting Anomalies in Edge Streams


## Summary

Randomized algorithm
Constant time

It mentions that the problem  is context dependent and must be analyzed in a specific context.

This article uses down sampling bursts of data

If an edge connects sparse parts of the graph it will marked like anomaly

In this article some sampling methods on streams mentioned that worth attention.

‍‍‍```
Reservoir sampling [14] is a classic algorithm to maintain
a fixed-size uniform sample of elements in a stream. Weighted
reservoir sampling [15] is used when elements are to be sampled
with different weights. When the stream contains edges
from a graph, several sampling mechanisms are available [16],
but none of them downsamples edges from bursty periods.
```



