# ML Case study: Weather Station Clustering using DBSCAN 


DBSCAN stands for **d**ensity-**b**ased **s**patial **c**lustering of **a**pplications with **n**oise**. It is a density-based clustering non-parametric algorithm: given a set of points in some space,
it groups together points that are closely packed together (points with many nearby neighbors), marking as outliers points that lie alone in low-density regions (whose nearest neighbors are too far away).

There are two key parameters of DBSCAN:

- **eps**: The distance that specifies the neighborhoods. Two points are considered to be neighbors if the distance between them are less than or equal to eps.

- **minPts**: Minimum number of data points to define a cluster.

Based on these two parameters, points are classified as core point, border point, or outlier:

- **Core point**: A point is a core point if there are at least minPts number of points (including the point itself) in its surrounding area with radius eps.
- **Border point**: A point is a border point if it is reachable from a core point and there are less than minPts number of points within its surrounding area.
- **Outlier**: A point is an outlier if it is not a core point and not reachable from any core points.

In this case study it is used DBSCAN to find the group of stations which show the same weather condition.
