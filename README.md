[DA5401] DA Lab - Assignment-5-DA25M014 Name - Jigarahemad K Shaikh, Roll Number: DA25M014

File needed for Evaluation - "DA5401_DA25M014_Assignment 5.ipynb"

Libraries Used - pandas, numpy, matplotlib (pyplot, patches, colors), seaborn, sklearn.preprocessing, sklearn.manifold

Color Palettes Used	- colorblind, Paul Tol (TOL_COLORS), Set1, Set2, husl, Spectral

Colormaps Used - Spectral (for heatmaps, violin plots)

🧠 Analysis and Discussion

🌐 Comparison of Global Structure Preservation

Isomap excels at revealing the global structure of the gene expression data.
It maintains long-range relationships between clusters, showing how the data manifold stretches and connects across the feature space.

The Isomap projection displays clusters as elongated, interconnected regions—preserving geodesic distances.
For example, the main clusters (C1 and ‘Other’) are often joined by a curving bridge, emphasizing their continuity within the manifold.
In contrast, t-SNE focuses on local neighbor preservation, sometimes compressing distant clusters into denser, misleading proximities to better show micro-structures.

🧬 Data Manifold Complexity and Classification

🌀 Concept of the Data Manifold

The data manifold is the hidden low-dimensional surface embedded in the 103-dimensional feature space where the data truly resides.
Algorithms like Isomap attempt to unfold this structure to reveal its true geometry in fewer dimensions.

🌊 Manifold Complexity (Curvature)

The Isomap visualization suggests a highly non-linear and curved manifold.
Clusters appear in arched or horseshoe shapes, indicating complex relationships that cannot be captured by linear projections.
This confirms that the gene expression space is intricately structured, requiring non-linear methods for faithful representation.

🎯 Relation to Classification Difficulty

The complexity of the data manifold directly explains why classification is difficult:

Linear models (e.g., Logistic Regression) assume flat decision surfaces → poor fit on curved manifolds.

Non-linear models (e.g., SVM with RBF kernel, Random Forests, Neural Networks) can adapt to twists and folds in the data, learning flexible decision boundaries.

Visible label mixing in t-SNE and strong curvature in Isomap confirm the hard-to-learn nature of this dataset.

💡 Key Insight:
The intertwined clusters, curved manifolds, and noisy label regions imply that robust, non-linear learning algorithms are essential for reliable performance.
This analysis connects data geometry to model design — bridging theory and practice in high-dimensional learning.

👇

🏁 Assignment Summary (High Level)

📊 Core Findings

Objective:
Visually identify noisy labels, outliers, and hard-to-learn samples using t-SNE and Isomap on standardized gene expression data.

🎯 t-SNE (Local View)

Revealed clear local clusters representing distinct functional groups.

Exposed regions of label intermixing, confirming ambiguous annotations and noisy samples.

Highlighted outliers — points far from any main cluster, indicating rare or erroneous cases.

🌐 Isomap (Global View)

Revealed that the data lies on a highly curved and complex manifold.

Preserved global distances and connectivity between major clusters.

Showed true topological separation between groups that appear compressed in t-SNE.

💡 Conclusion

The combination of high manifold complexity and label overlap confirms that
simple linear classifiers would perform poorly on this dataset.

Effective classification requires non-linear, flexible models such as
SVM (RBF), Random Forests, or Neural Networks —
algorithms capable of learning curved, intricate decision boundaries aligned with the true manifold geometry.

✨ t-SNE + Isomap together provide both microscopic and macroscopic insight — revealing how data behaves locally and globally across the complex biological landscape.


👇

📊 Detailed Analysis and Discussion (Low Level)

🧭 Comparison of Dimensionality Reduction Techniques

Both Isomap and t-SNE are powerful non-linear dimensionality reduction techniques, but they serve distinct purposes in visualizing high-dimensional gene expression data.
Understanding their comparative strengths is key to correctly interpreting the manifold structure.

📘 Isomap vs. t-SNE: Detailed Comparison
Aspect	Isomap	t-SNE
Primary Goal	Preserve global geodesic distances	Preserve local neighborhood similarity
Distance Metric	Geodesic distances via neighborhood graph	Probabilistic similarity between neighbors
Cluster Separation	Moderate; shows topology	Strong; highly distinct clusters
Distance Interpretation	Global distances meaningful	Distances between far clusters not interpretable
Global Structure	Excellent — preserves connectivity	Poor — distorts for local clarity
Local Structure	Moderate — blurs fine patterns	Excellent — sharp neighborhood grouping
Visualization Pattern	Stretched, interconnected clusters	Compact, well-separated clusters
Best Use Case	Understand overall geometry	Discover fine-grained local clusters
Computational Complexity	O(n²)–O(n³)	O(n²) with stochastic optimization

🌐 Global Structure Preservation

Isomap reveals the true large-scale connectivity of the data manifold.
Clusters appear stretched and interconnected, connected by bridges or curved paths that maintain meaningful geodesic distances.
In contrast, t-SNE compresses these distant relationships, prioritizing local detail over global accuracy.

🔍 Local Structure and Pattern Discovery

t-SNE excels at visual clarity — producing sharp, well-separated clusters that reveal subtle subpopulations.
Isomap instead provides a balanced yet less separated view — offering a more honest geometric depiction at the cost of some cluster visibility.

🧬 Data Manifold Complexity and Classification Implications

Concept of the Data Manifold

The data manifold is a low-dimensional curved surface embedded in the 103-dimensional space.
Algorithms like Isomap aim to “unroll” this surface to make its geometry interpretable.

Manifold Curvature and Complexity

Isomap visualizations show that yeast gene expression data lies on a highly curved, non-linear manifold — featuring arches, horseshoes, and overlapping structures.
This complexity signals strong inter-class relationships that linear methods cannot capture.

Impact on Classification Difficulty

Linear classifiers fail because they assume flat decision boundaries.

Non-linear models such as SVM (RBF), Random Forests, or Neural Networks are required to learn curved, intricate boundaries.

Mixing of colors in t-SNE and curvature in Isomap confirm the hard-to-learn nature of this dataset.

💡 Summary and Recommendations

When to Use Each Method

Use Isomap when:

Understanding global geometry is key.
Large-scale distances and connectivity matter.
Studying the manifold’s overall shape and curvature.

Use t-SNE when:

Identifying fine-grained clusters.
Exploring local neighborhoods.
Creating visually distinct 2D visualizations.


Key Insights for Classification

Manifold Complexity: The curved structure increases classification difficulty.
Model Selection: Non-linear models are essential for good performance.
Feature Engineering: Feature transformations may help linear models adapt.

Ensemble Methods: Combining non-linear learners often yields the best results.

🎯 Conclusion

Isomap and t-SNE offer complementary lenses into the yeast gene expression manifold:
Isomap uncovers global connectivity and geometric curvature,
while t-SNE clarifies local cluster structure.
Together they illustrate why this dataset demands non-linear, sophisticated learning models for accurate classification.

Date: 05/Oct/2025
