# Mechanism-of-Action Net (MoA-Net)

This is the code repository for the creation of MoA-Net and all of its variants.

All of the code is compartmentalized within Python notebooks. Thus, notebooks are ordered chronologically.

## Download MoA-net

To download MoA-net, access the specific versions from the following folders:

- [`data/kg/splits/MoA-net/`](https://github.com/enveda/neurosymbolic-mechanism/tree/main/data/kg/splits/MoA-net): The full, original MoA-net.
- [`data/kg/splits/MoA-net-permuted/`](https://github.com/enveda/neurosymbolic-mechanism/tree/main/data/kg/splits/MoA-net-permuted): The full, permuted version MoA-net, based on [XSwap](https://pubmed.ncbi.nlm.nih.gov/38323677/).
- [`data/kg/splits/MoA-net-protclass/`](https://github.com/enveda/neurosymbolic-mechanism/tree/main/data/kg/splits/MoA-net-protclass): The full version of MoA-net in which ~55% of the proteins have a protein subclass.


Within each of these folders, the following files can be downloaded:

```
kg_directory/
    ├── train.tsv
    ├── dev.tsv
    ├── test.tsv
    ├── kg_with_train_smpls.tsv
    ├── kg_no_cmp_bp.tsv
    ├── MARS/
        ├── ...
```
- `train.tsv`: The compound -> BP training triples (60%).
- `dev.tsv`: The compound -> BP validation triples (20%).
- `test.tsv`: The compound -> BP test triples (20%).
- `kg_with_train_smpls.tsv`: The MoA-net KG with the training triples from `train.tsv` included.
- `kg_no_cmp_bp.tsv`: The MoA-net KG with *no compound -> BP triples*. Therefore, it excludes all triples from `train.tsv`, `dev.tsv`, and `test.tsv`.
- The `MARS/` directory contains files which are processed and ready for input into MARS. These files are obtained after [the fifth notebook](notebooks/5_metapath_generation.ipynb), and their formats are specified in the `MARS` repository.


## Create MoA-net

To create MoA-net from scratch, the user can begin with [`0_preprocessing.ipynb`](https://github.com/enveda/neurosymbolic-mechanism/blob/main/notebooks/0_preprocessing.ipynb) and run each notebook, in order, until [`5_metapath_generation.ipynb`](https://github.com/enveda/neurosymbolic-mechanism/blob/main/notebooks/5_metapath_generation.ipynb). 

### Notes to the user:

- Notebook `5` is split into versions, based upon the version of MoA-net being used.
- Some large files should be downloaded from other sites to complete processing. Each notebook specifies the sources of such files.
- Notebooks beginning with `00` denote some preliminary searches which are not necessary to run.
- `MoA-Net-10k` is created as a result of MARS' automatic trimming step, but corresponding files can be found [here](data/kg/splits/MoA-net/10k/).