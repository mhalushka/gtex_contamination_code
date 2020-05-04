# gtex_contamination_code
The code used to generate the analyses used in "Consistent RNA Sequencing Contamination in GTEx and Other Datasets" by Nieuwenhuis et al. Now published in Nature Communications : https://www.nature.com/articles/s41467-020-15821-9
If there are any questions, concerns, or you require help running this code please contact Tim Nieuwenhuis at tnieuwe1@jhmi.edu or open an issue.
# Files and their purposes

### GTEx_file_maker_and_analysis.rmd:
This code is the main code of the paper as it generates the following analyses:
VST normalized data for every tissue
Clusters of highly variable genes for every tissue
The linear mixed models used in the paper to analyze the contamination of pancreas and esophagus mucosa genes
And the TPM density plot

This code should be easily able to run if the referenced data in the code is downloaded and put in ones directory. This code also required the making of sub directories such as /image_output and /data_output, to prevent the cluttering of the main working directory. 

Required files (all available through GTEx portal): 
GTEx_Analysis_2016-01-15_v7_RNASeQCv1.1.8_gene_tpm.gct,
All_Tissue_Site_Details.combined.reads.gct,
GTEx_v7_Annotations_SampleAttributesDS.txt

Note running this code can take a very long time due to DESeq2's VarianceStabilizingTransformation, as a result there is optional code to run the analyses with vst(), but note that these will not yield results accurate to those in the paper which used the full VarianceStabilizingTransformation. 

### tabula_muris_analysis.rmd

This code was written by Rohan X. Verma used to analyze how principal components in tabula muris can be effected by contamination.

### peer_factor_analysis.rmd

This code was written by Stephanie Yang, used to show how GTEx's batch effect removal strategy of PEER factors doesn't completely remove the effects of contamination from the dataset.

### other_analyses.rmd
This is a mix of code written by Tim Nieuwenhuis used to make various figures in the paper. Source data for all of this code can be found through the paper, however some of the data had to go through manipulations not included in this code. Please contact Tim Nieuwenhuis for explanation of the manipulations, data files used, and any other questions regarding this section. 
