# Celldega 16k Human PBMCs (Flex v2, TotalSeq-C 4-plex) DegaFiles

DegaFiles for the [Flex CITE-seq PBMC tutorial](https://broadinstitute.github.io/celldega/examples/tutorial_notebooks/Flex_CITE-seq_PBMC_Landscape-Clustergram-Enrich/) in the [Celldega](https://github.com/broadinstitute/celldega) documentation. Celldega's Landscape reads these files directly from this repository to color UMAPs of 12,242 cells by any gene or surface protein.

## Source data and attribution

These files are derived from the [16k Human PBMCs, TotalSeq-C 4-plex (Flex v2)](https://www.10xgenomics.com/datasets/Flexv2_16k_Human_PBMCs_TotalseqC_4plex) dataset, provided by 10x Genomics under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license.

## Changes from the source

The [pre-process notebook](https://huggingface.co/datasets/broadinstitute/Celldega_Supporting_Data/blob/main/Flex_16k_PBMC_CITE-seq/Flex_16k_PBMC_CITE-seq_Pre-process.ipynb) made these changes to Cell Ranger's multiplexed filtered feature-barcode matrix:

- named each surface protein by its target with a `_prot` suffix (for example, `CD4_prot`) so that proteins and genes with the same name stay distinct;
- wrote the raw gene and protein counts as DegaFiles: one Parquet file per feature with counts in `cbg/`, plus `cell_metadata.parquet`, `meta_gene.parquet`, and `landscape_parameters.json`.

The same counts, with sample assignments and antibody names, are in the companion MuData file, [`Flex_16k_PBMC_CITE-seq.h5mu`](https://huggingface.co/datasets/broadinstitute/Celldega_Supporting_Data/blob/main/Flex_16k_PBMC_CITE-seq/Flex_16k_PBMC_CITE-seq.h5mu), on Hugging Face.

## License

These derived files are shared under the same [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license as the source data; see [LICENSE](LICENSE).
