# Investigation of OpenFF types using MACE

## Environment (N.B. incompatible with  pytorch 2.6 or later)
mamba env create -f environment.yml

MACE can classify atomic environments using 3D information. The goal is to establish if it is possible to expand on existing (human curated) OpenFF types in a useful way?

mace_openff_types.ipynb first processes a small dataset and assigns OpenFF types, then embeds the same dataset using mace MACE. UMAP is then applied to these embeddings to create a 2D similarity plot, which is then clustered using HDBscan.

### Questions

- Does MACE find new types? i.e. Are there seperate UMAP clusters for the same OpenFF type (colour)?
- Are these types conformer independent? i.e. Are any atoms present in more than one UMAP cluster?
