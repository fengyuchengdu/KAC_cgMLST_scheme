# *Klebsiella aerogenes* complex cgMLST scheme

This is a chewBBACA generated cgMLST scheme used for typing *Klebsiella aerogenes* complex (KAC) species to clonal group (CG) level.

## Usage Instructions

1. Install [chewBBACA](https://chewbbaca.readthedocs.io/en/latest/).
2. Install [cgmlst-dists](https://github.com/B-UMMI/chewBBACA).
3. Pull all files in this repository.
4. Run AlleleCall in chewBBACA with the downloaded files. 
   Example command:
`chewBBACA.py AlleleCall -i /path/to/InputAssemblies -g /path/to/KAC_wgMLST -o /path/to/OutputFolderName --cpu 20 --genes-list KAC_cgMLST_2067`
5. Concatenate the output file named `results_alleles.tsv` with the pre-called dataset named `pre-called_cgMLST_dataset.tsv`.
6. Run cgmlst-dists on the combined dataset to obtain the pairwise cgMLST distances.
7. You may gather the distance matrix, using [csvtk](https://github.com/shenwei356/csvtk) or R, to find out the closest genome and the number of different loci in the pre-called dataset for each of your query genomes.
8. Check pre-defined CC for each pre-called genome and evaluate the distance using the pre-defined cutoff for CC determination.

## Citation

Please cite the following work when using this database:

Yu Feng, Yongqiang Yang, Ya Hu, Yuling Xiao, Yi Xie, Li Wei, Hongxia Wen, Linwan Zhang, Alan McNally, Zhiyong Zong. 2024. Population genomics uncovers the global distribution, antimicrobial resistance genes, and key virulence determinants of the opportunistic pathogen *Klebsiella aerogenes* (unpublished). Available at: [https://github.com/fengyuchengdu/KAC_cgMLST_scheme](https://github.com/fengyuchengdu/KAC_cgMLST_scheme)