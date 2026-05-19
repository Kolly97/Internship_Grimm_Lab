Chapter 5 is old Chapter 6
- created leave one out scatter plots
- created boxplot for leave one out for diff samples
- corr heatmap of randomized mouse


# Progress Log for Internship in AG Grimm
Author: Kolja Hildenbrand

Created: 2026-04-16

Latest Update: 2026-04-28


## Progress Log 

### 2026-05-05
- [ ] Adjusting figures according to meeting with Sabrina
    - [ ] 

### 2026-04-28
Chapter 3
- [x] rankshift scatter plot proportion with input?
    - [x] input -> gDNA
    - [x] input -> cDNA
    - [ ] maybe Proportion rankshift gDNA -> cDNA?
- [ ] Figures updaten with mean(log2) calculation
    - [x] a
    - [x] b
    - [x] c
    - [x] d

Chapter 5
- [ ] Figure e handlings updaten

General
- [ ] Writing figure captions




### 2026-04-27
Chapter 5
- [x]  Noise vs Abundance scatter (log - log)
    - [x]  x = mean abundance (z.B. input proportion oder mean counts)
    - [x]  y = variance oder |rep1 – rep2| oder std across replicates
    - [ ]  Aussage: Variants with low abundance exhibit substantially higher variability, demonstrating that sequencing noise is strongly dependent on signal strength.

Chapter 3
- [x] rankshift scatter plot proportion with input?
    - [x] input -> gDNA
    - [x] input -> cDNA
    - [ ] maybe Proportion rankshift gDNA -> cDNA?

### 2026-04-26
- [x] Chapter 5
    - [x] Randomize one mouse and use it in correlation matrix
    - [x] boxplot for randomized mouse
    - [x] Updated boxplot of leave one out vs biological
        - [x] excluded technical sample merge from liver samples 

### 2026-04-25
- [x] Corr matrix (Sample -> Mouse_ID -> Sex) (sns.clustermap?)
    - [x] liver
        - [x] gDNA
            - [x] technical
            - [x] biological
            - [x] sex
        - [x] cDNA
            - [x] technical
            - [x] biological
            - [x] sex
    - [x] heart
        - [x] gDNA
            - [x] biological
            - [x] sex
        - [x] cDNA
            - [x] biological
            - [x] sex
    - [x] box plot of correlations (technical rep | biological rep | sex)
    - [x] Leave one out scatter plot (shows that noise can be reduced by averaging)
        - [x] gDNA liver f2
        - [x] cDNA liver f2
        - [x] boxplot correlation of biological corr and leave one out correlation

### 2026-04-22
- [x] pooled sex has worse correlation with log2(mean(RPM_sample)/mean(RPM_input)) compared to mean(log2_enrichment)
- [x] Chapter 2.5 updated figures 
- [x] Chapter 3 updated figures
    - [ ] created new ECDF plot for Log2_enrichment_gDNA_to_cDNA
- [x] Chapter 4 figures
    - [x] Scatter plot
        - [x] Biological replicates
        - [x] Technical replicates
        - [x] Sex
                  
### 2026-04-21
- [x] Technical tables calculation and adding to df_long
- [x] Divide script_plots files in to each chapter to hold it a little bit less growded
- [x] extra table for long_sample, long_mouse_ID 
- [x] counts/RPM vs n_samples_present als boxplot von neuer df_pooled_log_of_mean
    - [ ] um es mit Counts zu machen muss ich counts in fd_pooled mitführen
- [x] df_pooled vs df_pooled_log_of_mean scatter plot
    - [ ] muss ich noch speichern
    - [ ] sehen sehr unterschiedlich aus

### 2026-04-20
**Table preperation**
- [x] neue df_pooled_log_of_mean mit log2(mean RPM ratio)
- [x] neue df_pooled_sex mit log2(mean RPM ratio)
- [x] Log2_enrichment_old beibehalten zum vergleichen#
- [x] Compare new Log2_enrichment to Log2_enrichment_old
- [x] save new tables for figures

          
### 2026-04-16      
- [x] Chapter 1: Rank shift proportion input library -> gDNA -> cDNA
    - [x] first calculating rank shift for each variant and than taking the mean of the rank
- [x] Chapter 6
    - [x] Column plot of variant number for just in 0 tissue -> in 6 tissue
    - [x] Boxplot distribution of enrichment in variants present in different amount of samples


### 2026-04-15
 - [x] Result Chapter 5
    - [x] Scatter plot
        - [x] Biological replicates
        - [x] Technical replicates
        - [x] Sex
- [x] Result Chapter 5
    - [x] AA position heatmaps for liver and heart
        - [x] input -> gDNA
        - [x] input -> cDNA
        - [x] gDNA -> cDNA
 - [x] Added original m2 NGS data to technical replicates
 - [x] Designed all my figures to make my work more efficient 
    

### 2026-04-14
- [x] Check for 4.5.1. to change it from no_pseudo to n_pseudo
    - [x] Not important since it uses proportion (notLog2_enrichment) and df_long
- [x] Result chapter 3
    - [x] Venn2 plot with top 10000 enrichment
    - [x] Diagramm of Venn2 plot overlap between top 1 and top 10^6 in log2 steps? (2,4,8,16,32,64,...)
    - [x] Rank_shift Log2_enrichment between gDNA and cDNA
    - [x] Heatmap of AA Position that influences log2_enrichment from gDNA to cDNA
        - [ ] per Mouse_ID with df_long instead of df_pooled


### 2026-04-13
- [x] Change save methode of pivot table in table prep script (by creating df_wide and reset index)
- [x] Result chapter 3
    - [x] Violin plot mean between biological replicate
    - [x] KDE plot for liver and heart (DNA and RNA in one plot, x = enrichment, y = n variant)

- [x] Result chapter 4
    - [x] ECDF plot of enrichment for liver and heart
          
- [x]  Update ReadMe with all needed plot
- [x]  Update plot script with all figures I want to create

### 2026-04-12
- [x] Create script for ECDF plot of proportion and Log2_enrichment
- [x] Change input library from extraction and tissue specific to only tissue specific
- [x] Re-calculate all samples of biological replicates
- [x] Calculate new Log2_enrichment from gDNA to cDNA for df_long_all_samples
      - Makes it possible to evaluate, which variants are especially good for transcription in cell
- [x] Create pivot table for AA_seq with proportion and enrichment both for gDNA and cDNA
- [x] recalculate technical replicates with liver spec input library instead of just raw library
- [x] Create new long table with all biological and technical replicates

### 2026-04-10
- [x]  Histogram proportion distribution with hue = mouse_id
- [x]  Venn2 figure for proportion chapter