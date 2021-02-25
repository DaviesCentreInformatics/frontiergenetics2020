# Analysis of river buffalo gene gains/losses and positive selection
The upstream synteny pipeline <https://gitlab.com/sandve-lab/salmonid_synteny> was run for 


river buffalo (GCF_003121395.1) (Low et al., 2019), goat (Capra hircus; GenBank accession no GCA_001704415.1) (Bickhart et al., 2017), pig (Sus scrofa; GenBank accession no GCA_000003025.6) (Warr et al., 2019), indicine cattle (Bos indicus; GenBank accession no GCA_003369695.1) (Low et al., 2020) , taurine cattle (Bos taurus; GenBank accession no GCA_002263795.1) (Rosen et al., 2020) and human (Homo sapiens; GenBank accession no GCA_000001405.39) (Schneider et al., 2017). 

This repository contains custom scripts 

to analyse the CAFE gene gain and losses results. 
These scripts have been used in paper "Adaptive signatures of river buffalo in protein degradation, olfactory receptor, detoxification and immune system". 
It also contains the MHC gene coordinates.

## CAFE gene gains and losses analysis
After running the synteny pipeline  that includes OrthoFinder, CAFE was done, after which the following was done:
1. Testing different models in CAFE, and choose the best model.
2. Importing CAFE results to perform GO, KEGG and Reactome enrichment analysis.
3. Find gene families with statistically significant gene gains/losses for all branches and river buffalo branch.

## PAML positive selection analysis

## MHC coordinates analysis
This script imported the blast results of Babesia ovata (GBE63528.1) against the six species genomes.
Calculate and visualize the blast hits for each species.
Additionally, the results of MHC were comapred to that obtained from manual curation. 
