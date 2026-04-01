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
485e6da
Script_for_table_prep.ipynb
