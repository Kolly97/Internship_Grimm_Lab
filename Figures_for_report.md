# Figures for Report of Internship in AG Grimm
Author: Kolja Hildenbrand

Created: 2026-04-15
Last Update: 



## Chapter 1: Successful in vivo transduction of AAV6-ML across tissues in mice
- [ ] Viral DNA detected across all tissues (Gel-Electrophoresis)
- [ ] Viral RNA indicate functional delivery (Gel-Electrophoresis)
- [ ] Sequencing library quality confirmed by bioanalyzer/gel electrophoresis

## Chapter 2: AAV6 Frequency changes indicates tissue and process specific in vivo selection 
- [x] Histogram with hue = Mouse ID
- [x] Venn2 of top 10000 Proportion in pooled sample and input library
    - [x] vllt mit Rankshift ersetzen
- [x] Rank shift proportion input library -> gDNA -> cDNA

## Chapter 2.5: Data coverage and variant representation across samples
- [x] Column plot of variant numbers that are in 0 samples, 1 samples, ..., 6 samples) (all in one plot)
    - [x] gDNA_liver
    - [x] cDNA_liver
    - [x] gDNA_heart
    - [x] cDNA_heart
- [x] Boxplot distribution of enrichment in variants present in different amount of samples
- [ ] Boxplot for counts per n_sample 0 - 6 (maybe I can see, that the variance is much better vor n >= 2)

## Chapter 3: RNA-level enrichment reflects stronger functional selection compared to DNA
- [x] Violin Plot between different tissues and extraction
- [x] KDE plot one per tissue, comparison gDNA vs cDNA
    - [ ] sagt eigentlich das selbe wie violin plot aus nur anschaulicher aber wenger statistic
    - [ ] Streichen?
- [x]  Venn2 of top 10,000 Log enrichment in min 2 samples
- [x]  Venn2 digramm from top 2 to top max variants
- [ ]  MA plot per tissue (for one mouse?)
    - [ ]  M = log2_enrichment_cDNA - log2_enrichment_gDNA
    - [ ]  A = mean(log2_enrichment_cDNA, log2_enrichment_gDNA)

## Chapter 4: Validation of reproducibility across technical and biological replicates
- [x] Scatter plot example
    - [x] Technical replicate (liver_m2 (technical rep specific library) vs liver_PCR)
    - [x] Biological replicate (m2 vs m1)
    - [x] sex against each other (male vs female)
- [ ] sns Heatmap  (maybe liver and heart together? But could be to crowded?)
    - [ ] gDNA
        - [ ] technical replicates 
        - [ ] biological replicates
        - [ ] sex replicates
    - [ ] cDNA
        - [ ] technical replicates 
        - [ ] biological replicates
        - [ ] sex replicates
- [ ] violin plot for correlation of gDNA (technical, biological, sex)
- [ ] violin plot for correlation of cDNA (technical, biological, sex)


## Chapter 5: Amino Acid specific position specific Log2_enrichment 
- [x] AA-position Heatmap Input -> gDNA
    - [x] liver
    - [x] heart
- [x] AA-position Heatmap Input -> cDNA
    - [x] liver
    - [x] heart
- [ ] AA-position Heatmap gDNA -> cDNA
    - [x] liver
    - [x] heart
- [ ] For supplementary figures heatmap of each mouse ID
  

## Chapter 6: Validation of correlation and detecting of noise
- [ ]  Noise vs Abundance scatter (log - log)
    - [ ]  x = mean abundance (z.B. input proportion oder mean counts)
    - [ ]  y = variance oder |rep1 – rep2| oder std across replicates
    - [ ]  Aussage: Variants with low abundance exhibit substantially higher variability, demonstrating that sequencing noise is strongly dependent on signal strength.
          
- [ ] Noise reduction by averaging (leave-one-out) (scatter plot)
    - [ ] Aussage: Averaging across biological replicates reduces stochastic noise and increases reproducibility of enrichment estimates.

- [ ] Randomize one mouse and use it in correlation matrix (f1)
    - [ ] Null model (shuffled correlation)
    - [ ] Scatter (real vs shuffled) + Histogram/Distribution of r
    - [ ] Shuffle Log2_enrichment innerhalb eines Samples (z. B. F1)
    - [ ] distribution of R über mehrere shuffel?
    - [ ] Aussage: Observed correlations are significantly higher than expected by random association, confirming that measured signals are biologically meaningful and not driven by noise.
        
- [ ] Correlation vs Pseudo Threshold (line-plot)
    - [ ] x: pseudo threshold (0,1,2,…)
    - [ ] y: Pearson r
    - [ ] getrennt für:
        - [ ] technical 
        - [ ] biological
        - [ ] sex (optional)
    - [ ] Aussage: Increasing filtering stringency (removal of pseudo-supported variants) improves correlation between replicates, indicating that low-confidence variants contribute disproportionately to noise.

- [ ] subsampling correlation
    - [ ] liver cDNA m1 vs m2 plot prozent daten 1% -> 100 % schauen was correlation und plotten


Chapter 1 – Transduction & QC

Chapter 2 – Coverage & variant representation

Chapter 3 – Tissue-specific selection

Chapter 4 – Functional enrichment (RNA vs DNA)

Chapter 5 – Reproducibility

Chapter 6 – Sequence-function landscape

Chapter 7 – Noise & method validation
