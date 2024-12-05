# Project Assignment B - Social Graphs and Interactions

## Explainer Notebook: Analyzing a Network of Scientists using Community Concepts

### Introduction

This notebook is part of Project Assignment B, where we analyze a real-world citation network from the SNAP dataset repository. Specifically, we are using the Hep-Th (High Energy Physics Theory) citation network, which represents the citation relationships among papers in the field of high-energy physics theory from the arXiv preprint platform.

Initially, our project aimed to construct and analyze a custom network of scientists across various fields by leveraging their h-index metrics, publication data, and citation relationships. We also intended to explore the complexity of the language used in their papers to uncover potential correlations between language sophistication and scientific influence. However, as we progressed, we faced significant challenges in accessing comprehensive and reliable publication data. Many APIs for fetching scientific metadata are either insufficient for our needs or require paid access, making the original idea unfeasible for this assignment.

To adapt, we shifted our focus to an existing, well-documented dataset: the Hep-Th citation network. This change allows us to focus on rigorous analysis without being set back by data accessibility issues.

### Objectives of the notebook:

- Construct and explore the Hep-Th citation network.
- Analyze the network structure to identify key properties such as centrality, density, and connected components.
- Detect and study communities within the network using community detection algorithms.
- Investigate the role of influential papers by analyzing their centrality measures.
- Analyze the descriptive text of each paper and comapre it's complexity with the number of citations.

### Dataset Information

The **Hep-Th** citation network is a directed graph where:
- Nodes represent papers in the high-energy physics theory domain.
- Edges indicate that one paper cites another.

The dataset spans from January 1993 to April 2003 and contains:
- 34,546 nodes (papers).
- 421,578 directed edges (citations).

This dataset is ideal for exploring citation dynamics, analyzing influential papers, and detecting communities within the field of high-energy physics.

### Analysis Steps

1. **Load Required Libraries**: Import necessary libraries for data processing, network analysis, and visualization.
2. **Construct the Citation Network**: Create a directed graph from the citation data.
3. **Assign Metadata to Nodes**: Process metadata files and assign them to corresponding nodes in the graph.
4. **Visualize the Network**: Generate a visualization of a sampled subgraph using the ForceAtlas2 layout.
5. **Compute Network Metrics**: Calculate key metrics such as density, clustering coefficient, and degree distribution.
6. **Identify Influential Papers**: Analyze in-degree to find the most cited papers (hubs).
7. **Community Detection**: Apply the Louvain algorithm and date-based grouping to detect communities and compare their modularity.
8. **Text Analysis**: Compute the Flesch Reading Ease score for the descriptive text of each paper and investigate its correlation with citation counts.
