# Internship_Grimm_Lab
Author: Kolja Hildenbrand

Created: 2026-04-01
Last Update: 2026-04-12

Progress of bioinformatic analysis of AAV6-ML NGS data processing and visualization. Collection of all code, script, tables and figures for internship. 

## Script for table preparation

1. [x] load csv tables
2. [x] translate Peptides -> AA_seq
    - [x] remove AA_seq with stop Codon
    - [ ] ❓ what should I do with AA = X (unknown AA)
4. [x] create list of all variants which are present in all samples in the same tissue
5. [x] create tissue specific library with frameshift (+1) and calculate proportion
    - [x] Change it to libraries that are tissue specific by merging cDNA and gDNA AA_seq
6. [x] add all tissue specific variants to sample, add frameshift (sum(count_sample)/sum(count_library)) and calculate proportion, cumulative proportion and log2_enrichment
7. [x] Create long table with all samples concentrated in one table (df_long_all_samples)
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


## Script for figures
0. Chapter 0: Getting a feeling for data
- [ ] Column plot of variant number for just in 0 tissue -> in 6 tissue
- [ ] Boxplot distribution of enrichment in variants present in different amount of samples

2. [x] Chapter 1: Comparison between input and samples regarding proportion
    - [x] Histogram with am propurtion with Hue = Sample -
    - [x] ECDF with samples and input
        - [x] refine code
        - [ ] ❓ Mean or median for axline?
    - [x] Venn2 Input vs mean proportion in sample -
        - [x] df_pooled umschreiben, damit ich auch pooled proportion habe
    - [ ] Rank shift proportion input library -> gDNA -> cDNA -

3. [x] Chapter 2: Comparison between biological replicates in enrichment
    - [x] ECDF plot -
        - [ ] ❓ Mean or median for axline?
        - [ ] ❓ Should I use with or without Pseudo? (Pseudo adds a log of varients with enrichment < 0)

4. [ ] Chapter 3: Comparison functional selection between RNA and DNA samples
    - [x] ⏳ Violin plot mean between biological replicate (*2024-04-13*) -
        - [ ] ❓ Variants in mind how many samples? ASK SABRINA
    - [x] KDE plot for liver and heart (DNA and RNA in one plot, x = enrichment, y = n variant) (*2024-04-13*) -
        - [ ] ❓ Variants in mind how many samples? ASK SABRINA
    - [x] Venn2 plot with top 10000 enrichment - 
        - [x] to show already the selection difference between biological step and tissue
        - [x] Shows in my opinion strong selection
    - [x] Diagramm of Venn2 plot overlap between top 1 and top 10^6 -
    - [x] Rank shift gDNA vs cDNA (maybe similar rank shift between tissues. shows that gDNA -> cDNA is a similar step and shows the same selectivity)
        - [x] ❓ maybe it's more clearly with AA_position heatmap for Log2_enrichment_gDNA_to_cDNA for both tissues?
        - [ ] ❓ maybe seperate for eaxh mouse ID instead of using df_pool?

5. [ ] Chapter 4: Log2 enrichment from gDNA level to cDNA level
       - [ ] ask Sabrina if this is relevant
   - [x] ECDF plot of enrichment for liver and heart (*2024-04-13*)
   - [x] ❓ AA_position heatmap for Log2_enrichment_gDNA_to_cDNA for both tissues (compare to show if there are specific motifs, that are good for transcription) - 

6. [ ] Chapter 5: Validation of reproducibility between biological and technical replicates
    - [ ] Scatter plot
        - [ ] ⏳ I have to check the Code again. the corr seems very bad for some samples
        - [x] Biological replicates - 
        - [x] Technical replicates - 
            - [x] Change df_long to include liver_original_rep
        - [x] Sex - 
        - [x] Try to include a filter to exclude pseudo variants (not so effective, makes corr worse everywhere exept for sex)
        - [ ] Try a better way to display correlation
    - [ ] Corr matrix (Sample -> Mouse_ID -> Sex) (sns.clustermap?) -
        - [ ] liver
        - [ ] heart
    - [ ] violin plot of correlations (technical rep | biological rep | sex) - 
    
7. Chapter 5: Validation of correlation and detecting of noise
    - [ ] Leave one out scatter plot (shows that noise can be reduced by averaging)
        - [ ] Use f1 mouse vs all the other
    - [ ] Randomize one mouse and use it in correlation matrix (f1)

8. [ ] Sex specific enrichment
    - [ ] MA Plot for sex specific?


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
    - [x] Send first draft of M&M to Sabrina
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

### 2026-04-16
- [ ] Corr matrix (Sample -> Mouse_ID -> Sex) (sns.clustermap?)
        - [ ] liver
        - [ ] heart
    - [ ] violin plot of correlations (technical rep | biological rep | sex)
    - [ ] Leave one out scatter plot (shows that noise can be reduced by averaging)
    - [ ] Randomize one mouse and use it in correlation matrix
- [ ] MA-plot for sex
    - [ ] liver
    - [ ] heart
- [ ] Chapter 1:
    - [ ] Rank shift proportion input library -> gDNA -> cDNA
- [ ] Chapter 6
    - [ ] Column plot of variant number for just in 0 tissue -> in 6 tissue
    - [ ] Boxplot distribution of enrichment in variants present in different amount of samples


### 2026-04-15
 - [ ] Result Chapter 5
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
- [ ]  




## Emojis:
[ ] = ToDo

[x] = done

⏳ = in progress

⚠️ = needs review

❓ = open question