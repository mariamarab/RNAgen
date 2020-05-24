# RNAgen

Recent advances in sequencing have allowed us to explore both the transcriptomic and epigenetic state of a cell. RNAGen uses Paired-seq data to generate scRNA-seq data that respects the chromatin accessibility of a cell.

## Features:
In each training iteration, we do the following, 
- Sample m positive examples {(atac_1, rna_1), (atac_2, rna_2), …, (atac_m, rna_m)}
- Define a normal distribution, and sample m noise samples {z_1, z_2, …, z_m}
- Obtain generated data {rna’_1, rna’_2, …, rna’_m}
- Sample m rna {rna^_1, rna^_2, …, rna^_m}
- Sample m atac {atac^_1, atac^_2, …, atac^_m}
- Update critic parameters
- Update generator parameters
 
## Installation Instructions:

### Dependencies:
Python 3.6

To install all required packages, run `python install -r requirements.txt`

Data should be transformed from scRNA data (barcodes, genes, matrix) to h5ad using the jupyter notebook provided and subsequently transformed to Tensorflow records (TFrecord) for manipulation by tensorflow. This last transformation happens in main.py with the process flag.

MulticoreTSNE is required to be compiled on your own machine. If on windows, visual studio build tools are needed to compile pip dependencies. If on Debian, build-essentials is needed. In any case, cmake is needed to build the dependencies.

## List of Team Members:
Mariam Arab

Ivan Perez

Mahdi Moqri

Adam Liang

Aleksis Korhonen

Gozde Buyukkahraman

Michael Disyak

Reva Shenwai

