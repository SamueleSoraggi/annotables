conda create -n anno-build -c conda-forge python=3.11 conda-build conda-verify anaconda-client
conda activate anno-build

#adapt channels below if needed
cd annotables
conda-build ./recipe -c conda-forge --output-folder /tmp/samuele/conda-build

anaconda login



anaconda upload -u hds.sandbox PATH-FROM-BUILD