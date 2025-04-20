# Paper Title: Topology and Data
## Author: Carlsson 2009
### Section 1. Introduction
#### Study Notes
* *...The mathematical formalism which has been developed for incorporating geometric and topological techniques deals with point clouds, ie. finite sets of points equipped with a distance function.*  
* *...The relationships which are useful involve continuous maps between the different geometric objects, and therefore become a manifestation of the notion $functoriality$, i.e, the notion that invariants should be related not just to objects being studied, but also the maps between these objects.*
#### Takeaways
The author attempted to approach big data from a topological perspective. Due to the ever-changing nature of data, high-dimensional and noisy data present more frequently than ever. In his opinion, methods inspired by topology can complement the limitations of geometric approaches. The followings are limitations for geometric methods and advantages of topological methods:

* **Metrics are not theoretically justified**  
For most geometric approaches, such as t-SNE and maniflod learning, it is necessary that the metric to use is clear and rigorous. In other words, the distance function shall satisfy the mathematical conditions. However, this is a strict assumption. In biology, the notion of distance or metric is rather ambiguous. For example, having the measurement of similarity between DNA sequences to be defined as "distance" is intuitive for biologists. However, it does not define a theoretically correct "metric". Interestingly, the geometric properties studied by topology is less sensitive to the choice of metric. What's more, for topology, it is the qualitative properties of the metrics that matter. The quantitative values of the metrics are replaced with the level of nearness between two points. This insensitivity is useful to the problems where metrics could only be defined in a coarse way. Please see [The topology of viral recombination among coronaviruses](/persistent_homology/README.md) for example. In this study, the measurement of similarity between DNA sequences is defined as the distance function. 
* **Coordinates are not natural**  
In physical world, coordinates are naturally defined as long as we are given the related information. However, even for data that could be expressed as the form of vectors, the data may not be embedded into any natural coordinate system. Take DNA sequences for example. For a DNA sequence with 10 nucleotides, say "ATGAACCTGT", it can be expressed in the form of a vector: [A, T, G, A, A, C, C, T, G, T]. But in which coordinate system can it fit naturally and intuitively? As a result, we have difficulties dealing with such situations with geometric methods. On the contrary, topology studies geometric object in a coordinate-free manner. Therefore, methods inspired by topology are suitable for the data which seem meaningless when embedded into any coordinate system. Please see [The topology of viral recombination among coronaviruses](/persistent_homology/README.md) for example.
* **Summaries are more valuable than individual parameter choices**  
Determining suitable thresholds for proper data analysis outcome is inevitable. To what extent can we beleieve the outcome if only a single theshold results in the desirable result? In other words, if the data analysis methods are too sensitive to parameter choices, the robustness of the outcome remains verification. From the other way around, to identify invariants and to summarize the corresponding behaviors under a change of parameters can be more valuable. From a topological perspective, functoriality of homological invariants may permit us to compute and summarize the invariants. Please see [The topology of viral recombination among coronaviruses](/persistent_homology/README.md) for example.

### Section 2. Persistent Homology
#### Study Notes
#### Takeaways
![diagram](/paper%20reading/tda_diagram.001.jpeg)
##### Basic concepts of homotopy
The notion of homotopy arises in the study of computable invariants of topological spaces. Given two topological spaces, say $X$ and $Y$,  we may want to define an equivalence relation which tells whether $X$ and $Y$ are equivalent. As a result, certain qualitative properties derived from the equivalence relation provides nice computable invariants for topological spaces. Homotopy is one of the concepts defining helpful equivalence relations. The ultimate purpose of homotopy is to define the notion of "homotopy equivalent" for two spaces. If two spaces are homotopy equivalent, several invariants will be derived, such as Betti numbers. In the following contents, mathematical definitions and examples will be provided to illustrate the fundamental concepts of homotopy.
* **Homotopic**: Two continuous maps $f,g:X\rightarrow Y$ are said to be homotopic if there exists a continuous map $H: X \times[0,1] \rightarrow Y $ such that $H(x, 0)=f(x)$ and $H(x,1)=g(x)$.
* **Homotopy equivalence**: For a continuous map $f:X\rightarrow Y$, if there exists a continuous map $g:Y\rightarrow X$ such that $f\circ g$ is homotopic to the identity map on $Y$ and $g\circ f $ is homotopic to the identity map on $X$.
* **Homotopy equivalent**:
Two spaces $X$ and $Y$ are said to be homotopy equivalent if there exists a map $f:X\rightarrow Y$ such that $f$ is a homotopy equivalence.
* **Examples**:
    * Any arbitrary continuous function $f: \mathbb{R} \rightarrow \mathbb{R}$, and a constant function $g:\mathbb{R}\rightarrow\mathbb{R}$, where $g(x)=0$ are homotopic.
        * $H(x,t) = (1-t)g(x) + tf(x) = tf(x) $ is continuous on $\mathbb{R}\times[0,1]$. [resource](#eg)
        * Such $f$ is a homotopy equivalence. For invertible functions, this is trivial. As for non-invertible functions, let us consider $g:\mathbb{R}\rightarrow \mathbb{R}$, where $g(x)=0$. Then, $g\circ f(x)=0,~\forall x \in \mathbb{R}$. Since arbitrary continuous functions, including the identity map, are homotopic to $g=0$, we have $g \circ f$ homotopic to the identity map on $\mathbb{R}$. Similarly, $f \circ g$ is homotopic to the identity map on $\mathbb{R}$. Hence, we proved that $f$ is a homotopy equivalence.
        * The equivalence relation $f$ partitions $\mathbb{R}$ into equivalence classes $\{[0]\}$.
        * Of course, we also derived a trivial statement, which is $\mathbb{R}$ and $\mathbb{R}$ are homotopy equivalent. 
##### Basic concepts of homology
##### Homology groups of simplicial complexes
##### Persistent homology
### Section 3. Imaging: Mapper
### Other Reference\Resources
<a id="eg"></a>
1. https://calculus123.com/wiki/Homotopy_and_homotopy_equivalence