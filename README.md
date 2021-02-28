# Analysis of river buffalo gene gains/losses and positive selection
This repository contains custom scripts used to prepare CAFE and PAML input and the associated output. 
A script for checking the MHC gene coordinates and Babesia blast hits is also included in the repository.
These scripts have been used in the paper "Adaptive signatures of river buffalo in protein degradation, olfactory receptor, detoxification and immune system". 

The synteny pipeline <https://gitlab.com/sandve-lab/salmonid_synteny> was used on six species as listed in the manuscript. The speciesMetadata_buffalo_20200729.yaml file to initiate this pipeline is given in this directory. 

## Table of Content
Inside the Buffalo folder, you will find the script in R markdown format and associated input and output files. As some scripts have dependencies on output from other scripts, it may be best to run the script in the order specified below.
### 1. CAFE_Match_gene_family.Rmd
  Group genes in the othrogroups into PANTHER gene families, and make a count table for gene families as CAFE input.
### 2. CAFE_Test_best_model.Rmd
  Choosing the best model to use for CAFE. 
### 3. CAFE_filter_buffalo_branch.Rmd
  Reading CAFE output and select the gene families with significant gene gains/losses for the buffalo branch.
### 4. CAFE_Find_immune_Gene.Rmd
  Using human and cattle annotations as the references to study the genes in the genes families with significant gene gains/losses for the buffalo branch. We target immune-related genes in these families for further analysis.
### 5. CAFE_GO_KEGG_Reactome_pathway.Rmd
  Importing CAFE results to perform GO, KEGG and Reactome enrichment analysis based on human and cattle annotations as the references.
### 6. PAML_branch_positive_selection.Rmd
  Applying the likelihood ratio test to select positively selected genes.
### 7. PAML_Find_immune_Gene.Rmd
  Searching immune-related genes in these positively selected genes using human database as the reference.
### 8. PAML_GO_KEGG_Reactome_pathway.Rmd
  Importing PAML results to perform GO, KEGG and Reactome enrichment analysis based on human and cattle annotations as the references.
### 9. Babesia_orf2_tblastn.Rmd 
  This script imports the blast results of _Babesia ovata_ (GBE63528.1) against the six species genomes.
  Calculate and visualize the blast hits for each species.
  Additionally, the results of MHC were compared to that obtained from manual curation (Babesia_orf2_tblastn.Rmd). 


Copyright 2021 Kelly Yan Ren

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
