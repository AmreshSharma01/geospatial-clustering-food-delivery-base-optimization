# Geospatial Clustering for Food Delivery Base Optimization

This project applies spatial clustering techniques to identify optimal base locations for a city-wide food delivery operation using restaurant location data. The analysis evaluates multiple clustering approaches and translates spatial patterns into actionable recommendations for delivery hub placement.

---

## Project Overview

Urban food delivery efficiency depends heavily on how well service bases are located relative to demand. In this project, restaurant locations are used as a proxy for delivery demand to:

- Identify spatial patterns in restaurant distribution
- Determine how many delivery bases are needed
- Recommend geographically optimal base locations
- Compare clustering methods for operational suitability

---

## Data Source

Restaurant location data was sourced from **OpenStreetMap (OSM)** and retrieved programmatically using the **OSMnx** Python library.  
Locations were filtered using the OpenStreetMap tag:{"amenity": "restaurant"}`

The study area was defined using city-level geographic boundaries, resulting in a georeferenced point dataset suitable for spatial analysis and clustering.

---

## Methodology

The project evaluates three clustering techniques commonly used in spatial analytics:

### K-Means Clustering
- Applied to latitude and longitude coordinates
- Optimal number of clusters determined using silhouette analysis
- Cluster centroids interpreted as candidate delivery base locations
- Provides stable, interpretable results suitable for operational planning

### DBSCAN
- Density-based clustering used to identify high-density restaurant regions
- Parameter tuning (`eps`, `min_samples`) performed using silhouette score grid search
- Effective for exploratory analysis and noise detection
- Less suitable for fixed base planning due to parameter sensitivity

### Hierarchical Clustering
- Agglomerative clustering used to explore spatial structure
- Evaluated with different linkage strategies
- Useful for understanding hierarchical relationships but less scalable for final base selection

---

## Visualization

Results were visualized using:
- Scatter plots for cluster structure comparison
- Silhouette score plots and heatmaps for parameter evaluation
- Interactive Folium maps to validate cluster geography and recommended base locations

---

## Tools & Technologies

- Python
- Pandas, NumPy
- Scikit-learn
- GeoPandas
- OSMnx
- Folium
- Matplotlib, Seaborn

---

## Key Findings

- K-Means clustering produced the most consistent and operationally meaningful clusters
- The optimal configuration resulted in **2 delivery bases**, balancing coverage and efficiency
- Cluster centroids provide geographically practical base locations
- DBSCAN and hierarchical clustering offered useful insights but were less suitable for final base planning

---

## Project Structure

├── spatial_cluster_analysis.ipynb
├── images/
└── README.md

---

## Conclusion

This project demonstrates how spatial clustering can support data-driven decision-making for urban delivery operations. Among the evaluated methods, K-Means clustering proved most effective for identifying delivery base locations due to its stability, interpretability, and direct mapping between clusters and service hubs.

The workflow presented here can be extended to other logistics, infrastructure planning, and location-allocation problems.

---

## Academic Note

This project is adapted from graduate-level coursework completed during a Master’s in Geomatics Engineering (University of Calgary).  
The repository has been refactored for portfolio and professional demonstration purposes.  
No assignment instructions, grading criteria, or solution keys are included.

---

## Author

**Amresh Sharma**  
Geospatial / GIS Analyst & Developer



