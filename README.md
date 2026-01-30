# Energy & Sustainability Patterns in Ohio  
### Unsupervised Learning Analysis

This project explores county-level energy composition patterns across Ohio using unsupervised learning techniques.  
Rather than prediction, the focus is on discovering structure, similarity, and dominant energy archetypes across counties.

Publicly available EIA-923 and EIA-860 datasets are used to analyze electricity generation by fuel type and geography.

---

## Project Objectives

- Explore Ohio’s electricity generation landscape at the county level  
- Identify dominant energy-generation profiles across regions  
- Apply unsupervised learning to uncover latent structure  
- Compare clustering results across multiple algorithms  

---

## Data Sources

- **EIA-923**: Plant-level electricity generation data  
- **EIA-860**: Power plant metadata  

The datasets were merged at the plant level and aggregated to construct county-level fuel composition profiles.

---

## Methodology

### 1. Data Preparation
- Merged generation and plant metadata
- Filtered to Ohio plants
- Aggregated net generation by county and fuel type
- Grouped fuel codes into interpretable categories:
  - Coal  
  - Natural Gas  
  - Nuclear  
  - Renewables  
  - Other fuels
- Constructed fuel-share features 

### 2. Exploratory Data Analysis
- Fuel mix distributions (linear & log scale)
- County-level generation disparities
- Spatial concentration of fuel types

### 3. Feature Engineering
- County × fuel-group feature matrix
- Standardization using `StandardScaler`
- Dimensionality reduction for visualization and clustering

### 4. Unsupervised Learning Techniques
- PCA 
- t-SNE
- K-Means clustering
- K-Medoids clustering
- Hierarchical clustering (Ward linkage)

Cluster validity was assessed using:
- Elbow method
- Silhouette scores
- Cophenetic correlation (hierarchical clustering)

---

## Key Findings

- Ohio counties consistently cluster into five energy archetypes:
  1. Renewables-dominant  
  2. Natural-gas–dominant  
  3. Coal-dominant  
  4. Nuclear-dominant  
  5. Mixed-profile energy systems  

- Results were stable across K-Means, K-Medoids, and Hierarchical clustering, indicating robust underlying structure.
- Energy generation is highly geographically concentrated, with a small number of counties accounting for most production.
- Nuclear and coal generation are extremely localized, while renewables and natural gas are more widespread.

---

## Visualizations

- Fuel mix bar charts (linear & log scale)
- County-level heatmaps
- PCA scree plots and component projections
- t-SNE embeddings across multiple perplexities
- Ohio county maps colored by cluster assignments
- Stacked bar charts of cluster energy composition

---

## Tools & Libraries

- **Python**
- pandas, numpy
- scikit-learn, scikit-learn-extra
- matplotlib, seaborn
- scipy
- geopandas

---

## Project Scope & Notes

This is an exploratory analysis intended to surface structural patterns rather than make causal or policy claims.  
The results provide a foundation for future extensions, such as:
- Temporal energy transitions
- Policy-relevant comparisons
- Infrastructure planning insights

---

## Repository Contents

