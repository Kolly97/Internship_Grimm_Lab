# Internship_Grimm_Lab
Author: Kolja Hildenbrand

Date: 01/04/2026

Progress of bioinformatic analysis of AAV6-ML NGS data processing and visualization. Collection of all code, script, tables and figures for internship. 

## Script for table preparation

1. [x] load csv tables
2. [x] translate Peptides -> AA_seq 
3. [x] create list of all variants which are present in all samples in the same tissue
4. [x] create tissue specific library with frameshift (+1) and calculate proportion
    - [x] Change it to libraries that are tissue specific by merging cDNA and gDNA AA_seq
5. [x] add all tissue specific variants to sample, add frameshift (sum(count_sample)/sum(count_library)) and calculate proportion, cumulative proportion and log2_enrichment
6. [x] Create long table with all samples concentrated in one table (df_long_all_samples)
    - [x]Calculate Log2_enrichment_gDNA_to_cDNA (for chapter 4)
8. [x] Create pooled table by merging all mouse_ID together and
    - [x]calculate mean log2_enrichment
    - [x]calculate mean Proportion
    - [x]calculate mean Log2_enrichment_gDNA_to_cDNA
    - [x]track in how many samples the variant is present 
10. [x] Create Pivot Table with all enrichment and proportion values
11. [x] Save all the tables


## Script for technical replicates

1. [x] Create lists
2. [x] Load tables
    - [x] raw library
    - [x] technical replicates
    - [ ] long table with biological replicates
3. [ ] Load, translate and remove AA_seq with stop_codon from samples
- [ ] with old read out script
- [ ] save raw AA tables
4. [ ] Create tissue and gDNA/cDNA specific input library with frameshift +1
5. [ ] Calculate proportion and log2_enrichment for samples with frameshift + (sum(count_sample)/sum(count_input))
6. [ ] Create long table of technical replicates and combine with biological replicates
    - [ ] Add column 'replicate' to mark if sample is a biological or technical replicate
    - [ ] change it to Replicate
7. [ ] Save technical replicates and long table with biological and technical replicates


## Script for plots

1. [x] Comparison between input and samples regarding proportion
    - [x] Histogram with am propurtion with Hue = Sample
    - [x] ECDF with samples and input
        - [ ] refine code 
    - [x] Venn2 Input vs mean proportion in sample
        - [x] df_pooled umschreiben, damit ich auch pooled proportion habe

2. [x] Comparison between biological replicates in enrichment
    - [x] ECDF plot

3. [ ] Comparison functional selection between RNA and DNA samples
    - [ ] Violin plot mean between biological replicate
    - [ ] KDE plot for liver and heart (DNA and RNA in one plot, x = enrichment, y = n variant)
    - [ ] Venn2 plot with top 10000 enrichment
        - [ ] to show already the selection difference between biological step and tissue
    - [ ] Diagramm of Venn2 plot overlap between top 1 and top 10^6

4. [ ] Plots for enrichment between DNA to RNA?
   - [ ] ask Sabrina if she thinks this is relevant

5. [ ] Validation of reproducibility between biological and technical replicates
    - [ ] Scatter plot
        - [ ] Biological replicates
        - [ ] Technical replicates
        - [ ] Sex 
    - [ ] Corr matrix (Sample -> Mouse_ID -> Sex) (sns.clustermap?)
        - [ ] liver
        - [ ] heart
    - [ ] violin plot of correlations (technical rep | biological rep | sex)
    - [ ] Leave one out scatter plot (shows that noice can be reduced by averaging)
    - [ ] Randomize one mouse and use it in correlation matrix

   

7. [ ] AA position specific log2_enrichment
    -[ ] maybe


