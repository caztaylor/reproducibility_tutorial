# reproducibility_tutorial
FOSS 2020
    1  cd /scratch
    2  df -h
    3  git clone https://github.com/caztaylor/reproducibility_tutorial.git
    4  ls
    5  clear
    6  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    7  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
    8  ln -s /opt/conda/pkgs/*/bin/* /bin
    9  ln -s /opt/conda/pkgs/*/lib/* /usr/lib
   10  /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
   11  /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
   12  /opt/conda/bin/pip install bash_kernel
   13  /opt/conda/bin/pip install ipykernel
   14  /opt/conda/bin/python3 -m bash_kernel.install
   15  clear
   16  /opt/conda/bin/conda search R
   17  /opt/conda/bin/conda search -bioconda htseq
   18  /opt/conda/bin/conda search -c bioconda htseq
   19  clear
   20  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   21  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility_tutorial/'
   22  /opt/conda/bin/conda search -c bioconda snakemake
   23  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   24  ln -s /opt/conda/bin/* /bin
   25  ln -s /opt/conda/lib/* /usr/lib
   26  snakemake --version
   27  sudo apt-get update
   28  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   29  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   30  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
   31  sudo apt-get update
   32  sudo apt-get install -y docker-ce docker-ce-cli containerd.io
   33  docker run hello-world
   34  cd /scratch/reproducibility-tutorial/
   35  cd /scratch/reproducibility_tutorial/
   36  history
   37  history >> README.md
