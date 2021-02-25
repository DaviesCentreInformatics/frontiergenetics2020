# Analysis of river buffalo gene gains/losses and positive selection
The upstream synteny pipeline <https://gitlab.com/sandve-lab/salmonid_synteny> that includes OrthoFinder was run for six species.

The repository contains custom scripts used to prepare the CAFE and PAML analysis materials and analyse their outputs following the synteny pipeline.
A script checking the MHC gene coordinates and Babesia blast hits also included in the repository.
These scripts have been used in the paper "Adaptive signatures of river buffalo in protein degradation, olfactory receptor, detoxification and immune system". 


## CAFE gene gains and losses analysis

After running the synteny pipeline, the following was done as ordered before and after CAFE analysis:
1. Group genes in the othrogroups into PANTHER gene families, and make a count table for gene families as CAFE input (CAFE_Match_gene_family.Rmd).
2. Dealing with the output of multiple error-control models for CAFE and choose the best model (CAFE_Test_best_model.Rmd).
3. Reading cafe output and select the gene families with significant gene gains/losses for the buffalo branch (CAFE_filter_buffalo_branch.Rmd).
4. Using human and cattle annotation as the reference to study the genes in the genes families with significant gene gains/losses for the Buffalo branch. To be more specific, checking the immune-related genes in those families (CAFE_Find_immune_Gene.Rmd).
5. Importing CAFE results to perform GO, KEGG and Reactome enrichment analysis base on human and cattle annotation as the reference (CAFE_GO_KEGG_Reactome_pathway.Rmd).

## PAML positive selection analysis

The cds sequences of single-copy othrogroups were collected from OrthoFinder to perform PAML analysis, and results were analysed as following steps:
1. Applying the likelihood ratio test 2[log(Likelihood_Alternative_hypothesis) - log(Likelihood_Null_hypothesis)] to select significantly positive-selected sites (PAML_branch_positive_selection.Rmd).
2. Searching the immune-related genes in those positive-selected sites with the human database as the reference (PAML_Find_immune_Gene.Rmd).
3. Importing PAML results to perform GO, KEGG and Reactome enrichment analysis base on human and cattle annotation as the reference (PAML_GO_KEGG_Reactome_pathway.Rmd).

## Babesia and MHC coordinates blast analysis
This script imported the blast results of Babesia ovata (GBE63528.1) against the six species genomes.
Calculate and visualize the blast hits for each species.
Additionally, the results of MHC were comapred to that obtained from manual curation (Babesia_orf2_tblastn.Rmd). 

The whole repository can be git cloned and reproduced.
