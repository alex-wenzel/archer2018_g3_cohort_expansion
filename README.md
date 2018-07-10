# g3_cohort_expansion

**Author**: Clarence Mah<br>
**Email**: ckmah@ucsd.edu

TODO: citation

This replicates the "Group 3 Cohort Expansion" analysis found in: Proteomics, post-translational modifications, and integrative analyses reveal heterogeneity of molecular mechanisms within medulloblastoma subgroups. Archer et al. (2018).

To expand our number of G3a/G3b type tumors (typed with proteomics-based clustering), we used the c1 and c5 samples from the Cho et al. (2011) cohort which are most like Group 3. Since only array data were available for the Cho samples, we also used array data for our current Group 3 cohort to better normalize the two data sets.

Following the methods in Cho et al. (2011), we projected the expression data for both cohorts into “gene set space” using a single sample version of GSEA (ssGSEA), using the Hallmarks (H), Curated Gene Sets (C2), Motif Gene Sets (C3), and Oncogenic Gene Sets (C6) collections from the MSigDB. Using the G3a, G3b labels for the current cohort, we determined the 10 most differentially enriched gene sets for each subtype (Figure S5D, main text) according to the Information Coefficient (IC) as defined in Kim et al. (2016). These top sets were used as features to train a Bayesian cumulative log-odds predictor as previously described (Tamayo et al., 2011). The predictor was applied to the projected Cho et al. (2011) c1 and c5 samples to assign G3a and G3b labels.

Open the Jupyter notebook found at [notebook/Group 3 Cohort Expansion Bayesian Classifier Analysis.ipynb](notebooks/Group%203%20Cohort%20Expansion%20Bayesian%20Classifier%20Analysis.ipynb) to access the analysis.
