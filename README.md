# Genetic-data-rearrangement
Rearrangement algorithms for genetic data

## Introduction
This script is to prerocess the genomic data in MS format for CNN classification.

## Help
The C code can be compiled by the command:

``gcc Extract.c -o ms2txt -lm``

Then, the in-tool help will be printed by using command:

``./ms2txt -H``

```
This program is to process raw genetic data in MS format by reordering binary data.

Required flag:
	-i: path to input ms file (str)
	-o: path to output folder (str), automatically create if it doesn't exist
	-a: rearrangement algorithm that will be executed firstly (int), it requires one of the following values
		0: Original-no-sorting
		1: Row-decreasing-hamming-weight
		2: Row-decreasing-decimal-value
		3: Row-decreasing-correlation
		4: Row-increasing-hamming-distance
		5: Row-hamming-weight-increasing-hamming-distance
		6: Column-decreasing-derived-allele-frequency
		7: Column-decreasing-correlation
		8: Column-decreasing-minor-allele-frequency
		9: Column-decreasing-minor-allele-frequency-with-bit-flipping
		10: Column-decreasing-hamming-distance
		11: Column-adjacent-max-correlation
		12: Column-adjacent-max-correlation-on-different-sides
	-b: rearrangement algorithm that will be executed secondly (int), it requires one of the following values
		0: Original-no-sorting
		1: Row-decreasing-hamming-weight
		2: Row-decreasing-decimal-value
		3: Row-decreasing-correlation
		4: Row-increasing-hamming-distance
		5: Row-hamming-weight-increasing-hamming-distance
		6: Column-decreasing-derived-allele-frequency
		7: Column-decreasing-correlation
		8: Column-decreasing-minor-allele-frequency
		9: Column-decreasing-minor-allele-frequency-with-bit-flipping
		10: Column-decreasing-hamming-distance
		11: Column-adjacent-max-correlation
		12: Column-adjacent-max-correlation-on-different-sides
	-h: number of samples (int)
	-w: number of SNPs to be extracted (int)
```

For _win2img.py_, the following command can be used.

``python win2img.py --help``

The generated message is the following.

```
This script can be executed for converting the .txt files of the binary matrices into images.

The: -i, -h, -w, -o, -f, -m flags are required
	-d: path to an input folder containing the .txt files of the binary matrices (str)
	-h: the height of the images (int)
	-w: the width of the images (int)
	-o: path to an output folder (str)
	-f: the stored format (str), "pdf" or "png" (def: png)
	-m: color mode (str), "black", "grey" or "RGB" (def: black)
```
