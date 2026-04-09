# Internship_Grimm_Lab
Author: Kolja Hildenbrand

Date: 01/04/2026

Progress of bioinformatic analysis of AAV6-ML NGS data processing and visualization. Collection of all code, script, tables and figures for internship. 

## Script for table preparation

1. load csv tables
2. translate Peptides -> AA_seq 
3. create list of all variants which are present in all samples in the same tissue and extraction type
4. create tissue and extraction specific library with frameshift (+1) and calculate proportion
5. add all tissue and extraction typical variants to sample, add frameshift (sum(count_sample)/sum(count_library)) and calculate proportion, cumulative proportion and log2_enrichment
6. Create long table with all samples concentrated in one table (df_long_table)
7. Create pooled table by merging all mouse_ID together and calculate mean log2_enrichment and in how many samples each variant is present
8. Save all the tables

## Script for plots
1. Comparison between input and samples regarding proportion
- Histogram with am propurtion with Hue = Sample
- ECDF with samples and input
- Venn2 Input vs mean proportion in sample

2. Comparison between biological replicates in enrichment
- ECDF plot

3. Comparison functional selection between RNA and DNA samples
- Violin plot mean between biological replicate
- KDE plot for liver and heart (DNA and RNA in one plot, x = enrichment, y = n variant)
- Venn2 plot with top 10000 enrichment
    - to show already the selection difference between biological step and tissue
- Diagramm of Venn2 plot overlap between top 1 and top 10^6

4. Plots for enrichment between DNA to RNA?
- ask Sabrina if she thinks this is relevant

5. Validation of reproducibility between biological and technical replicates

6. AA position specific log2_enrichment
- maybe

## Script for technical replicates
1. Create lists
2. Load tables
- raw library
- technical replicates
- long table with biological replicates
3. Load, translate and remove AA_seq with stop_codon from samples
- with old read out script
- save raw AA tables
4. Create tissue and gDNA/cDNA specific input library with frameshift +1
5. Calculate proportion and log2_enrichment for samples with frameshift + (sum(count_sample)/sum(count_input))
6. Create long table of technical replicates and combine with biological replicates
7. Save technical replicates and long table with biological and technical replicates