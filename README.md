# *Klebsiella aerogenes* complex cgMLST scheme

This is a chewBBACA generated cgMLST scheme used for typing *Klebsiella aerogenes* complex (KAC) species to clonal group (CG) level.

## Recipe

1. Install [chewBBACA](https://chewbbaca.readthedocs.io/en/latest/).
2. Install [cgmlst-dists](https://github.com/B-UMMI/chewBBACA).
3. Pull all files in this repository.
4. Run AlleleCall in chewBBACA with the downloaded files. 
   Example command:
`chewBBACA.py AlleleCall -i /path/to/InputAssemblies -g /path/to/KAC_wgMLST -o /path/to/OutputFolderName --cpu 20 --genes-list KAC_cgMLST_2066 --training-file KAC_training.trn`
5. Concatenate the output file named `results_alleles.tsv` with the pre-called dataset named `pre-called_cgMLST_dataset.tsv`.
6. Run cgmlst-dists on the combined dataset to obtain the pairwise cgMLST distances.
7. You may gather the distance matrix, using [csvtk](https://github.com/shenwei356/csvtk) or R, to find out the closest genome and the number of different loci in the pre-called dataset for each of your query genomes.
8. Check pre-defined CG for each pre-called genome and evaluate the distance using the pre-defined cutoff for CG determination.

## Citation

Feng Yu, Zong Zhiyong. 2024. A cgMLST scheme for *Klebsiella aerogenes* complex species (unpublished). https://github.com/fengyuchengdu/KAC_cgMLST_scheme
