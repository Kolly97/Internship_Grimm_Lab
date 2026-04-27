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
- [x] Boxplot for RPM per n_sample 0 - 6 (maybe I can see, that the variance is much better vor n >= 2)
    - [x] yes it seems like all variants below this line are to much influenced by pseudo measurments

## Chapter 3: RNA-level enrichment reflects stronger functional selection compared to DNA
- [x] Violin Plot between different tissues and extraction
    - [ ] muss ich nochmal mit mean (log2_enrichment) machen

- [x]  Venn2 of top 10,000 Log enrichment in min 2 samples
- [x]  Venn2 digramm from top 2 to top max variants
- [x]  ECDF plot for Log2_enrichment_gDNA_to_cDNA
- [ ]  correlation oder rankshift proportion with input?

- [x] KDE plot one per tissue, comparison gDNA vs cDNA

## Chapter 4: Validation of reproducibility across technical and biological replicates
- [x] Scatter plot example
    - [x] Technical replicate (liver_m2 (technical rep specific library) vs liver_PCR)
    - [x] Biological replicate (m2 vs m1)
    - [x] sex against each other (male vs female)
- [x] sns Heatmap  (maybe liver and heart together? But could be to crowded?)
    - [x] gDNA
        - [x] technical replicates
            - [x] corr with liver_origin_rep compared to liver_m2 is just a little bit better for gDNA and the same for cDNA
        - [x] biological replicates
        - [x] sex replicates
    - [x] cDNA
        - [x] technical replicates 
        - [x] biological replicates
        - [x] sex replicates
- [x] violin plot for correlation of gDNA (technical, biological, sex)
- [x] violin plot for correlation of cDNA (technical, biological, sex)

## Chapter 5: Validation of correlation and detecting of noise
- [x]  Noise vs Abundance scatter (log - log)
    - [x]  x = mean abundance (z.B. input proportion oder mean counts)
    - [x]  y = variance oder |rep1 – rep2| oder std across replicates
    - [x]  Aussage: Variants with low abundance exhibit substantially higher variability, demonstrating that sequencing noise is strongly dependent on signal strength.
    - [ ]  Have to check what I am blotting and to make sure, that I use /RPM for cv
          
- [x] Noise reduction by averaging (leave-one-out) (scatter plot)
    - [x] Aussage: Averaging across biological replicates reduces stochastic noise and increases reproducibility of enrichment estimates.
- [x] boxplot of correlation for biological vs. leave-one-out

- [x] Randomize one mouse and use it in correlation matrix (f1)
    - [x] Null model (shuffled correlation)
    - [x] Shuffle Log2_enrichment innerhalb eines Samples (z. B. F1)
    - [x] distribution of R über mehrere shuffel?
    - [x] Aussage: Observed correlations are significantly higher than expected by random association, confirming that measured signals are biologically meaningful and not driven by noise.

## Chapter 6: Amino Acid specific position specific Log2_enrichment 
- [ ] AA-position Heatmap Input -> gDNA
    - [ ] liver
    - [ ] heart
- [ ] AA-position Heatmap Input -> cDNA
    - [ ] liver
    - [ ] heart
- [ ] AA-position Heatmap gDNA -> cDNA
    - [ ] liver
    - [ ] heart
- [ ] For supplementary figures heatmap of each mouse ID



Chapter 1 – Transduction & QC

Chapter 2 – Coverage & variant representation

Chapter 3 – Tissue-specific selection

Chapter 4 – Functional enrichment (RNA vs DNA)

Chapter 5 – Reproducibility

Chapter 6 – Sequence-function landscape

Chapter 7 – Noise & method validation
