# Real-data demonstration: Bayesian LP with posterior feasibility (PBMC3k)

## Dataset
- Scanpy PBMC3k processed scRNA-seq dataset (clusters via Louvain).

## Task
- Select a gene panel of size B=30 maximizing between-cluster separation score.
- Posterior-feasibility constraint: for each cluster, expected detectable genes among selected >= L=8.0 across posterior scenarios.

## Posterior certificate

|   alpha_intent |   B_panel |   L_required |   S_scen_optim |      M_cert |   posterior_violation_hat |   posterior_violation_UB95 |
|---------------:|----------:|-------------:|---------------:|------------:|--------------------------:|---------------------------:|
|       0.050000 | 30.000000 |     8.000000 |     300.000000 | 4000.000000 |                  0.020500 |                   0.024582 |

## Cluster-wise certificate detail

| cluster           |   mean_coverage |   p5_coverage |   p50_coverage |   p95_coverage |   viol_rate_cluster |
|:------------------|----------------:|--------------:|---------------:|---------------:|--------------------:|
| B cells           |          8.2080 |        8.0535 |         8.2073 |         8.3666 |              0.0088 |
| CD14+ Monocytes   |         10.0433 |        9.9253 |        10.0432 |        10.1572 |              0.0000 |
| CD4 T cells       |          8.1233 |        8.0344 |         8.1254 |         8.2114 |              0.0120 |
| CD8 T cells       |         12.5638 |       12.3876 |        12.5633 |        12.7383 |              0.0000 |
| Dendritic cells   |         14.2745 |       13.7620 |        14.2721 |        14.8075 |              0.0000 |
| FCGR3A+ Monocytes |         11.6428 |       11.4021 |        11.6411 |        11.8892 |              0.0000 |
| Megakaryocytes    |         13.0598 |       12.2098 |        13.0531 |        13.8803 |              0.0000 |
| NK cells          |         14.4419 |       14.2103 |        14.4407 |        14.6698 |              0.0000 |

## Selected gene panel

|   rank | gene     |   x_relaxed |   score_w |
|-------:|:---------|------------:|----------:|
|      1 | MPP1     |      1.0000 |    3.2303 |
|      2 | TPM4     |      1.0000 |    2.2407 |
|      3 | NCOA4    |      1.0000 |    1.9361 |
|      4 | GPX1     |      1.0000 |    1.4630 |
|      5 | MARCH2   |      1.0000 |    1.3891 |
|      6 | ODC1     |      1.0000 |    1.2855 |
|      7 | FERMT3   |      1.0000 |    1.1597 |
|      8 | GZMB     |      1.0000 |    1.1905 |
|      9 | PRF1     |      1.0000 |    1.0731 |
|     10 | FGFBP2   |      1.0000 |    1.0736 |
|     11 | NKG7     |      1.0000 |    1.0101 |
|     12 | CCL5     |      1.0000 |    0.9317 |
|     13 | MFSD1    |      1.0000 |    0.9729 |
|     14 | CTSW     |      1.0000 |    0.8454 |
|     15 | LTB      |      1.0000 |    0.4619 |
|     16 | HLA-DQA1 |      1.0000 |    0.9499 |
|     17 | PTPRCAP  |      1.0000 |    0.5268 |
|     18 | CST7     |      1.0000 |    0.9070 |
|     19 | IL32     |      1.0000 |    0.4851 |
|     20 | GZMA     |      1.0000 |    0.9013 |
|     21 | SPON2    |      1.0000 |    0.9157 |
|     22 | SAT1     |      1.0000 |    0.6345 |
|     23 | ARPC1B   |      1.0000 |    0.4888 |
|     24 | S100A6   |      1.0000 |    0.4267 |
|     25 | HLA-DQB1 |      1.0000 |    0.8031 |
|     26 | MCUR1    |      1.0000 |    0.8250 |
|     27 | CYBA     |      1.0000 |    0.4017 |
|     28 | CST3     |      1.0000 |    0.6953 |
|     29 | COTL1    |      0.9579 |    0.4778 |
|     30 | AIF1     |      0.8020 |    0.6415 |

## Figures generated
- heatmap_cluster_means_selected_genes.png
- panel_gene_scores.png
- posterior_coverage_boxplot.png
- posterior_violation_hist.png
- umap_clusters.png
- umap_gene_GPX1.png
- umap_gene_MARCH2.png
- umap_gene_MPP1.png
- umap_gene_NCOA4.png
- umap_gene_ODC1.png
- umap_gene_TPM4.png
