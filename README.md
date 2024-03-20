# Mechanism-of-Action Net (MoA-net)

This is the code repository for the creation of MoA-net and all of its variants.

All of the code is compartmentalized within Python notebooks. Thus, notebooks are ordered chronologically.

## Download MoA-net

To download MoA-net, access the specific versions from the following folders:

- [`data/kg/splits/MoA-net/`](https://github.com/enveda/neurosymbolic-mechanism/tree/main/data/kg/splits/MoA-net): The full, original MoA-net.
- [`data/kg/splits/MoA-net-protclass/`](https://github.com/enveda/neurosymbolic-mechanism/tree/main/data/kg/splits/MoA-net-protclass): The full version of MoA-net in which ~55% of the proteins have a protein subclass.

Within each of these folders, the following files can be downloaded:
- `train.tsv`: The compound -> BP training triples (60%).
- `dev.tsv`: The compound -> BP validation triples (20%).
- `test.tsv`: The compound -> BP test triples (20%).
- `kg_with_train_smpls.tsv`: The MoA-net KG with the training triples from `train.tsv` included.
- `kg_no_cmp_bp.tsv`: The MoA-net KG with *no compound -> BP triples*. Therefore, it excludes all triples from `train.tsv`, `dev.tsv`, and `test.tsv`.


## Create MoA-net

To create MoA-net from scratch, the user can begin with [`0_preprocessing.ipynb`](https://github.com/enveda/neurosymbolic-mechanism/blob/main/notebooks/0_preprocessing.ipynb) and run each notebook, in order, until [`5_metapath_generation.ipynb`](https://github.com/enveda/neurosymbolic-mechanism/blob/main/notebooks/5_metapath_generation.ipynb).

The user should note that notebook `5` is split into versions, based upon the version of MoA-net being used.

### Notes:

- Notebooks beginning with `00` denote some preliminary searches which are not necessary to run.
- Notebooks beginning with `99` denote archived notebooks which were experimental, but no longer used.
- Notebooks `6`-`8` can be run after model results are obtained.