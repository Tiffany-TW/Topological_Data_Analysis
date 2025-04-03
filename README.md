# Topological_Data_Analysis
This repository contains theoretical concepts and practical implementation of topological data analysis methods, including persistent homology, mapper, and etc.. 

## An overview
### Introduction
Topological data analysis (abbreviated as TDA) is a method that provides us the shape of given data. Based on algebraic topology, TDA describes the shape of data without dimensionality reduction. Therefore, it is especially suitable for analyzing high-dimensional data. According to different theoretical concepts in algebraic topology, there are many ways that are used to describe data shape, including persistent homology, Mapper, and etc. 
### Comparison with common dimension reduction methods
When it comes to dimensionality reduction methods, PCA, t-SNE, and manifold learning are the most commonly known. In addition to dimensionality reduction, revealing clustering of the instances of the given data is also one of the major functions. Similarly, TDA describes the shape of data cloud by providing clustering information. However, PCA, t-SNE, and manifold learning are often accompanied with information loss while TDA guarantees less information loss. Moreover, TDA is more robust to noise of data (See persistent homology).
## Topics
### [Persistent Homology](/persistent_homology/README.md)
### [Mapper](/mapper/README.md)
## Applications
* **Identification of the shape of data**: TDA has been broadly applied to various fields such as finance, biology, smart manufacturing [[1]](#ref) and etc.
* **Connections to machine learning methods**
* **Visualization**: TDA allow us to visualize high-dimensional data in low dimensional image without projecting data into low dimensional space.

## Reference
1. Uray, M., Giunti, B., Kerber, M., & Huber, S. (2024). Topological Data Analysis in smart manufacturing: State of the art and future directions. Journal of Manufacturing Systems, 76, 75-91.
2. [Carlsson, G. (2009). Topology and data. Bulletin of the American Mathematical Society, 46(2), 255-308.](/paper%20reading/carlsson.md)