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