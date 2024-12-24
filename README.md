# FormanRicciAnalysis

This repository provides a Python implementation for computing and visualizing Forman-Ricci curvature on a directed, weighted graph. Using the NetworkX library, this project analyzes edge-level properties of a graph to understand its local geometric and structural properties.

## Features
- Constructs a weighted, directed graph with predefined nodes and edges.
- Calculates Forman-Ricci curvature for each edge using the formula:

  \[
  F(e) = w_e \left( \frac{w_{v_1}}{w_e} - \sum_{e_{i, v_1} \sim e} \frac{w_{v_1}}{\sqrt{w_e w_{e_{i, v_1}}}} \right) + w_e \left( \frac{w_{v_2}}{w_e} - \sum_{e_{o, v_2} \sim e} \frac{w_{v_2}}{\sqrt{w_e w_{e_{o, v_2}}}} \right)
  \]

  Where:
  - **w_e**: Weight of the edge.
  - **w_{v_1}** and **w_{v_2}**: Weights of the source and target nodes of the edge.
  - **e_{i, v_1}**: Incoming edges to the source node.
  - **e_{o, v_2}**: Outgoing edges from the target node.

- Visualizes the graph with curvature values annotated on each edge.
- Offers a custom node layout for improved clarity in visualization.

## Example Graph Visualization
Below is an example of the graph generated by the script, with Forman-Ricci curvature values displayed on the edges.

![Graph Visualization with Forman-Ricci Curvature](graph_visualization.png)

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/<your_username>/FormanRicciAnalysis.git
   cd FormanRicciAnalysis
   ```
2. Install the required dependencies:
   ```bash
   pip install networkx matplotlib
   ```
3. Run the script:
   ```bash
   python main.py
   ```
4. The output graph will be displayed, showing the Forman-Ricci curvature values for each edge.

## Applications
- **Network Analysis:** Identify dense clusters and sparse regions in the graph.
- **Edge-Level Insights:** Understand bridge edges and local connectivity.
- **Visualization:** Provide graphical representations of curvature for research and analysis.

## References
This implementation and the simplified formula for Forman-Ricci curvature are based on adaptations and interpretations found in the following works:

1. Forman, R. "Bochner's Method for Cell Complexes and Combinatorial Ricci Curvature." Discrete & Computational Geometry, 2003. [Link](https://link.springer.com/article/10.1007/s00454-002-0760-1)
2. Ni, C.C., Lin, Y.Y., Gao, J., Gu, X., & Saucan, E. "Ricci curvature of the Internet topology." INFOCOM, 2015. [DOI](https://doi.org/10.1109/INFOCOM.2015.7218428)
3. Sreejith, R.P., Jost, J., Saucan, E., & Samal, A. "Forman curvature for directed networks." [arXiv](https://arxiv.org/abs/1605.04662)
