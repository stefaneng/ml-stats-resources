# Distance Functions

## Distance Measures

The requirements for a distance measure are:
  - Non-negativity: dist(a,b) >= 0
  - Identity of indiscernibles: dist(a,b) = 0 iff a = b
  - Symmetry: dist(a,b) = dist(b,a)

And a distance measure satisfies:
  - dist(a,b) <= dist(a,c) + dist(c,b)

## Similarity Measures
Methods for comparing the differences between points which do not satisfy the requirements for distance measures

### References
  - [A Survey of Distance and Similarity Measures Used Within Network Intrusion Anomaly Detection](http://ieeexplore.ieee.org/xpls/abs_all.jsp?arnumber=6853338)