# GWAS on the North American Rheumatoid Arthritis Consrtium
> BS859 Final Project Option 2
**Author**: Johnathan Zhang


## Background Information on the Genetics of Rheumatoid Arthritis
> All information/instructions copied from project instructions

The HLA region on 6p21 has been implicated in RA by numerous studies, and there is consistent evidence that HLA-DR alleles contribute to disease risk. 
HLA-DR is an MHC class II cell surface receptor encoded by the human leukocyte antigen complex on chromosome 6 region 6p21.31. 
The 'shared epitope' hypothesis was proposed by Gregersen et al. (1987) to explain the organization of risk for rheumatoid arthritis from DR alleles. 
According to this hypothesis, individuals who share the amino acid QK/RRAA motif in positions 70-74 of the DR molecule show an increased risk for disease.
This model was not quite sufficient to explain risk according to DR types and a newer model utilizing data from positions 70-74 has been developed (du Montcel et al., 2005).

Specific autoantibodies are noted to co-occur with rheumatoid arthritis. 
Rheumatoid factor IgM is a measure of active disease correlated with erosive arthritic disease. 
However, a more newly identified autoantibody, anti-cyclic citrullinated peptide (anti-CCP), is more specific for the disease and is a better predictor of erosive outcome (Huizanga et al., 2005). 
Elevations of anti-CCP have been noted to predict increased risk for development of rheumatoid arthritis (Kroot et al., 2000)

## Software requirements
- Plink 1.9
- Plink 2.0
- GMMAT 
- smartpca for PCA
- R 4.3.0
- METAL for meta-analysis
- LDSC python2 package for LD score regression



## Project Instructions
### 1. Data Cleaning of the NARAC GWAS data
Perform genetic data cleaning of the NARAC GWAS data. 
Then, perform PCA on the data to identify study outliers, and create a set of PCs that can be used in association analyses. 
- In your write up, state and justify the analyses you did and in what order, and how many individuals and SNPs you removed and retained at each step. 
- Provide your recommendations on which PCs to include in case-control GWAS analyses, and explain your choice.

### 2. Identify genetic associations with disease case status 
It is well known that the HLA region on chromosome 6p21 plays an important role in RA. 
It is also well known that females are affected by RA much more frequently than males. 
Your goals are to determine if there are additional genomic regions (in addition to the HLA region on chromosome 6) that are associated with RA in females in this sample, and to determine whether any of the regions are sex-specific. 
For all analyses, be sure to state and justify the significance criteria you use.

#### 2A. Split the GWAS by sex 
Perform two genome-wide association analyses for rheumatoid arthritis: one using only female subjects, and one using only male subjects. 
Explain how you chose covariates, and how you accounted for population structure (or, if you chose not to account for population structure, justify your decision). 
Present a written summary of your results with appropriate plots and tables that describe your findings.

#### 2B. GWAS Meta-analysis with Metal
Perform a genome-wide meta-analysis that combines the male-only and female-only results with a test for heterogeneity. 
Present a written summary of your findings, including appropriate plots and tables, and be sure to address the questions: do males and females show association in the same regions? 
Do the significantly associated SNPs appear to have similar effects in males as in females? 
Discuss the limitations of the data and the methods you used.

### 3. LD Score Regression
Use LD score regression and the Okada et al summary statistics to 1) estimate the heritability of RA, and 2) compare the heritability in the Asian and European populations.
Describe your methods (including all assumptions you’ve made) and present and explain your results.
