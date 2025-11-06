# GitGood Repository
## I see different fontsize.
A repository to learn git.

1. How to get good version control using git when running pip publish or conda publish?

 - If you have a python-implemented program, and you want to use it with conda-installed packages. I recommend publishing it as pip package again, but when using it, create the conda environment as usual. Introduce the **python**, **pip** and **setuptools** version compatible with the program, and install that program once you finished creating it. 

 - When running the part requiring conda-installed packages, you can use either ``os.systems()`` or ``subprocess.process`` to run the command. 

 - There are many examples in metagenomics: using ``prodigal, bedtools and HMMER`` that are not commonly pip-installable.

2. If you are designing a conda-based package, commonly the code is a mix of languages, like Rust, Julia, C and Python. When trying to initiate the publication, ask ``Gemini`` or ``ChatGPT5`` to get familiarize with writing .github yml files doing the working pipelines to publish to Anaconda/miniconda. 

 - When using such package, install it via conda, and add any other packages or pip installable packages via adding ``pip:`` inside the ``conda_env.yaml``.

- ``Note``: when using conda environment and activating it, the $PATH points to the ``bin/`` directory inside the conda environment, and thus the python version is pointed to there. For example: ``home/path/to/envs/comebin_env/bin/python`` is the python inside your comebin_env in your spartan. When activating it, installation using ``pip`` will add the packages to the ``lib/python/site-packages``. While running mamba or conda will add packages to the conda libs.

3. Our next step is trying to incorporate low-level languages like ``Rust`` and ``C++`` to python, thus trying to do some basic stuffs. A good example is Karpathy's ``nanochat`` repository combining generative models with a rust-encoded tokenizer. 

## A map between architectures and biological problems:
1. All-aspect models.
- encoder-only: ViT, nucleotide transformer and LucaVirus, generate latent representations of biological sequences. ``Note``: Vision models like ViT can also serve for biological purposes like taxonomic predictions using skinny genomic sequencing data: VarCoder.
   
- decoder-only: detr, deformable detr, mask2former, EVO1/2 and ESM2/3, generate biological sequences to fulfil purposes such as designing the artificial phi T4 bacteriophage.

2. Protein structural prediction, design and generation
- RFdiffusion: David baker-designed diffusion transformer that designs a protein resembling a natural one and gives its structure. 
- Alphafold3: structural prediction for given amino acid sequences, can be visualized by pyMOL.
- Coupled with GPU-accelerated MMseq2

3. Genomic elements effect, QTL prediction, transcriptomics
- Enformer, predict non-coding DNA's effects on gene expression with long context, as well as promoter-enhancer interactions. 
- Borzoi, predicts the contribution to the transcript level (coverage) by regulatory elements.
- Alphagenome, variant-effect prediction with up to 1M genomic window as inputs. 

4. Cell-state predictor, scRNAseq and virtual cells
- State: predict perturbation effects of changing one gene/set of genes on a cell.
- C2S: multi-modal model with a transformer architecture, run on the RNAseq matrix to decode the tissues, perturbation styles.
- NicheFormer: predict the cell identity and niche based on the input data (might be the RNAseq matrix). 

5. VAE
- scanpy, scvi: generate embeddings that work for UMAP clustering, showing the improvement on cell-type profiling and removal of batch effects in scRNAseq.
- A series of metagenomic binners: LorBin and VAMB, generates latent embeddings to cluster microbial genomes.

6. RNA language model
- CodonFM: NVIDIA-developed RNA language modeller. 


