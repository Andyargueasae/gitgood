# GitGood Repository
## I see different fontsize.
A repository to learn git.

1. How to get good version control using git when running pip publish or conda publish?

 - If you have a python-implemented program, and you want to use it with conda-installed packages. I recommend publishing it as pip package again, but when using it, create the conda environment as usual. Introduce the **python**, **pip** and **setuptools** version compatible with the program, and install that program once you finished creating it. 

 - When running the part requiring conda-installed packages, you can use either ``os.systems()`` or ``subprocess.process`` to run the command. 

 - There are many examples in metagenomics: using ``prodigal, bedtools and HMMER`` that are not commonly pip-installable.