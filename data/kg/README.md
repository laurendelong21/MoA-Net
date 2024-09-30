# KG Files and Variants

Within the [splits folder](splits/), we have different KGs to work with:

- [`data/kg/splits/MoA-net/`](data/kg/splits/MoA-net/): The full, original MoA-net.
- [`data/kg/splits/MoA-net-permuted/`](data/kg/splits/MoA-net-permuted/): The full, permuted version MoA-net, based on [XSwap](https://pubmed.ncbi.nlm.nih.gov/38323677/).
- [`data/kg/splits/MoA-net-protclass/`](data/kg/splits/MoA-net-protclass/): The full version of MoA-net in which ~55% of the proteins have a protein subclass.
- [`data/kg/splits/Hetionet/`](data/kg/splits/Hetionet/): The [Hetionet KG](https://het.io/), which was used in the [PoLo paper](https://github.com/liu-yushan/PoLo).


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

All other files are generated or necessary at some point during KG creation (running the notebooks).