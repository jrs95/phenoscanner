# phenoscanner <img src="man/figures/logo.png" align="right" height="139"/>
R package to query the PhenoScanner database of human genotype-phenotype associations.  

## Functions
* `phenoscanner`: this function allows users to query the PhenoScanner database.  

## Installation
```
install.packages("remotes")
remotes::install_github("jrs95/phenoscanner")
```

## Examples
```
# Library
library(phenoscanner)

# SNP
res <- phenoscanner(snpquery = "rs10840293")
head(res$results)
res$snps

# Gene
res <- phenoscanner(genequery = "SWAP70")
head(res$results)
res$genes

# Region  
res <- phenoscanner(regionquery = "chr11:9685624-9774538")
head(res$results)
res$regions

# Multiple SNPs
res <- phenoscanner(snpquery = c("rs10840293", "rs10"))
head(res$results)
res$snp
```

## Citations
* Staley JR, *et al.* PhenoScanner: a database of human genotype-phenotype associations. [Bioinformatics](https://pubmed.ncbi.nlm.nih.gov/27318201/) 2016;32(20):3207-3209.  
* Kamat MA, *et al.* PhenoScanner V2: an expanded tool for searching human genotype-phenotype associations. [Bioinformatics](https://pubmed.ncbi.nlm.nih.gov/31233103/) 2019;35(22):4851-4853.  

## Terms of use
Please abide by the [terms of use](http://www.phenoscanner.medschl.cam.ac.uk/about/#terms) of PhenoScanner when using this R package.  
