# Sound clustering assignment – ML techniques II

This project applies **unsupervised clustering techniques** on an **unlabeled sound dataset**, using Mel Spectrogram features for dimensionality reduction and cluster discovery.

## Project Structure

```
sound_clustering_assignment/
├── README.md              
├── data/                    
├── notebook/             
│   └── sound_clustering_assignment.ipynb             
```

## Tasks performed

### Feature extraction
- Extracted features from `.wav` files using **Mel Spectrograms**.
- Computed statistical descriptors (mean & std) from each Mel frequency band.
- Logged and skipped corrupt files using exception handling.

### Raw feature visualization
- Visualized raw features using scatter plots and pairplots.
- Observed no visible clusters due to high-dimensional redundancy.

### Dimensionality reduction
- Applied **PCA** and **t-SNE** to project features into 3D space.
- **t-SNE** revealed clearer cluster separation compared to PCA.

### Clustering (K-Means & DBSCAN)
- Evaluated optimal number of clusters using **Elbow** and **Silhouette** methods.
- Compared clustering performance:
  - K-Means (k=4): moderate separation.
  - DBSCAN: better-defined and denser clusters.

### Evaluation metrics
- Used **Silhouette Score**, **Davies-Bouldin Index**, and **Calinski-Harabasz Score** to assess clustering quality.
- DBSCAN outperformed K-Means on this dataset.

## Conclusion

Dimensionality reduction was crucial due to the high-dimensional feature space from Mel spectrograms. **t-SNE** provided more interpretable visualizations. **DBSCAN** handled the noisy structure of audio data better than K-Means, highlighting the importance of algorithm choice in unsupervised learning.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/g-tumwesigye/sound_clustering_assignment.git

   
