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
    - [x] Calculate Log2_enrichment_gDNA_to_cDNA (for chapter 4)
8. [x] Create pooled table by merging all mouse_ID together and
    - [x] calculate mean log2_enrichment
    - [x] calculate mean Proportion
    - [x] calculate mean Log2_enrichment_gDNA_to_cDNA
    - [x] track in how many samples the variant is present 
10. [x] Create Pivot Table with all enrichment and proportion values
11. [x] Save all the tables


## Script for technical replicates

1. [x] Create lists
2. [x] Load tables
    - [x] raw library
        - [x] maybe liver specific library
    - [x] technical replicates
    - [x] long table with biological replicates
3. [x] Load, translate and remove AA_seq with stop_codon from samples
- [x] with old read out script
- [x] save raw AA tables
4. [x] Create tissue specific input library with frameshift +1
5. [x] Calculate proportion and log2_enrichment for samples with frameshift + (sum(count_sample)/sum(count_input))
6. [x] Create long table of technical replicates and combine with biological replicates
    - [x] Add column 'replicate' to mark if sample is a biological or technical replicate
    - [x] change it to Replicate
7. [x] Save tables
    - [x] technical replicates
    - [x] long table with biological and technical replicates


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
    - [ ] Leave one out scatter plot (shows that noise can be reduced by averaging)
    - [ ] Randomize one mouse and use it in correlation matrix

   

7. [ ] AA position specific log2_enrichment
    - [ ] maybe

## Writing the Report
1. [x] Title page
   
3. [ ] Abstract
   - [ ] First draft
         
4. [ ] Table of Content
   - [x] Created
         
5. [ ] Abbreviation
    - [x] Created
          
3. [ ] Introduction
   - [ ] Create structure
   - [ ] First draft
   - [ ] Send first draft of Introduction to Sabrina
   - [ ] First draft of Aims of Introductions
   - [ ] Revise your text using Sabrina's suggestions
   - [ ] Send first draft of Aims to Sabrina
   - [ ] Revise Aims using Sabrina's suggestions
         
4. [ ] Materials & Methods
    - [x] Created chapters
    - [x] Created Devices table
    - [x] Created Software table
    - [x] Created Kits table
    - [x] Created Consumables table
    - [x] Created Reagents table
    - [x] Created cells table
    - [x] Created Enzymes table
    - [x] Created Buffers table
    - [x] Create tables for PCR and cDNA synthesis process 
    - [x] First draft of text
    - [ ] Send first draft of M&M to Sabrina
    - [ ] Revise M&M using Sabrina's suggestions

5. [ ] Results
    - [ ] Create Plots (See *Script for Plots*)
    - [ ] Create figure captions
        - [ ] Figure caption chapter *proportion*
        - [ ] Figure caption chapter *log2_enrichment*
        - [ ] Figure caption chapter *Comparison functional selection between RNA and DNA samples*
        - [ ] Figure caption chapter *biological vs technical replicates*
        - [ ] Figure caption chapter *log2_enrichment from gDNA to cDNA*
    - [ ] Send plots to Sabrina
    - [ ] Discuss plots with Sabrina
    - [ ] Write first draft for Results
        - [ ] Chapter *proportion*
        - [ ] Chapter *log2_enrichment*
        - [ ] Chapter *Comparison functional selection between RNA and DNA samples*
        - [ ] Chapter *biological vs technical replicates*
        - [ ] Chapter *log2_enrichment from gDNA to cDNA*

7. [ ] Discussion
    - [ ] Collect first ideas and bulletpoints for discussion
    - [ ] Connect statements I want to make

## Progress Log 

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
- [ ]  




### Emojis:
[x] = done
⏳ = in progress
⚠️ = needs review
❓ = open question