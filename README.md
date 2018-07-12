# Anaerobic digesters

This repository contains a series of notebooks and data to reproduce the
analyses in Vazquez-Baeza et al. 20XX. However, the sequencing data is not
included here, instead we only include processed files (feature tables,
metadata tables, phylogenetic tree, etc.). For access to the raw and quality
controlled sequences, please refer to Qiita study
[11282](https://qiita.ucsd.edu/study/description/11282).

The notebooks are grouped in 6 main sections: normalization, diversity
analyses, heatmap visualization, ordination, metric comparison, and
environmental classifier.

# Normalization

These notebooks detail how we identified the *Acinetobacter* that we used for
count normalization. Namely [taxonomic
selection](notebooks/0.1.1-acinetobacter-identification.ipynb), [sequence
similarity filtering](notebooks/0.1.2-acinetobacter-selection.ipynb),
[normalization](notebooks/0.1.3-acinetobacter-normalization.ipynb), and
[visualization](notebooks/0.1.3.1-acinetobacter-visualizations.ipynb).

# Diversity

With the normalized count table we proceeded to [calculate alpha and
beta](notebooks/0.2.0-processing-alpha-and-beta.ipynb) diversity statistics.
Additionally, we use the alpha diversity measurements to [compare against the
environmental variables](notebooks/0.2.1-alpha-diversity-correlations.ipynb).

# Heatmaps

To visualize the amplicon sequence variants (ASVs), we hierarchically clustered
the per-ASV trajectories over the 4 different digesters and represented them
as a [heatmap](notebooks/0.3.0-heatmaps.ipynb).

# Ordinations

In order to integrate the microbial and the chemical information, we used a
constrained and an unconstrained ordination. In the [constrained ordination](
notebooks/0.4.0-cca-biplot.ipynb) we use the chemical data, while in the
[unconstrained ordination](notebooks/0.4.1-pcoa-biplot.ipynb) we use the
phylogenetic information and the microbial data alone.

# Metric comparison

In order to assess the effect of normalizing the data we computed 5 distance
matrices, and [compared their normalized and
non-normalized](notebooks/0.5.0-metric-wide-comparison.ipynb) versions using
Mantel's test.

# Environmental classifier

Lastly, we combined the dataset with a subset of samples from the [Earth
Microbiome Project](http://www.earthmicrobiome.org/) (EMP) and created a
[sample classifier](notebooks/0.6.0-distance-classification-to-the-emp.ipynb)
based on the environmental labels from the EMP.
