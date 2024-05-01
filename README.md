# Whole-person function terminologies for Mobility and Self-Care and Domestic Life

This repository contains terminologies for whole-person function, described in the LREC paper `A Whole-Person Function Dictionary for the Mobility, Self-Care and Domestic Life Domains: a Seedset Expansion Approach`, https://aclanthology.org/2022.lrec-1.305/.

Both terminologies contain the seedset terms used for expansion, and the expanded terms using medical resources, lexicons, and clustering using word embeddings, as described in the paper.
The seedset is based on manually annotated data from the Biomedical Translational Research Information System (BTRIS) at the National Institutes of Health Clinical Center and from Social Security Administration (SSA) Consultative Examination documents.

The terminologies contain the terms and their associated ICF code(s). All terms and ICF codes have been verified by domain experts. For more information, we refer to the paper.

## Citing this work

Please cite the LREC submission:

> Ayah Zirikly, Bart Desmet, Julia Porcino, Jonathan Camacho Maldonado, Pei-Shu Ho, Rafael Jimenez Silva, and Maryanne Sacco. 2022. A Whole-Person Function Dictionary for the Mobility, Self-Care and Domestic Life Domains: a Seedset Expansion Approach. In _Proceedings of the Thirteenth Language Resources and Evaluation Conference_, pages 2850–2855, Marseille, France. European Language Resources Association.

## Getting started
The terminologies are stored as tab-separated files, and contain a commented line with license info and a column header.

Example code to extract a list of terms using Python:
```
tsv_path = "terminology_scdl.tsv"

# Using pandas
import pandas
df = pandas.read_csv(tsv_path, encoding="utf-8", sep="\t", comment="#")
terms = list(df.term)

# Without pandas
with open(tsv_path, "r", encoding="utf-8") as f:
    # Ignore first two lines (license comment and header)
    terms = [line.split("\t")[0] for line in f.readlines()[2:]]
```
