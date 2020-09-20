# foss2020
A repository for the Cyverse FOSS 2020 experience

## Computer Setup






## Set up repository
    1  cd /scratch
    2  ls
    3  df
    4  git clone https://github.com/tonyva/foss2020.git
    5  ls
    6  cd foss2020/
    7  ls

## Set up MiniConda
    8  cd .. ; wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
    9  bash Miniconda3-latest-Linux-x86_64.sh 
   10  bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda
   11  ls -l /root
   12  rm -r /root/miniconda3/
   13  ln -s /opt/conda/pkgs/*/bin/* /bin
   14  ln -s /opt/conda/pkgs/*/lib/* /usr/lib

## Install Jypyer lab
   15    /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
   16  /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0
   17  /opt/conda/bin/pip install bash_kernel
   18  /opt/conda/bin/pip install ipykernel
   19  /opt/conda/bin/python3 -m bash_kernel.install
   20  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'
   21  /opt/conda/bin/jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/foss2020/'

## Install snakemake
   22  /opt/conda/bin/conda search -c bioconda snakemake
   23  /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1
   24  ln -s /opt/conda/bin/* /bin
   25  ln -s /opt/conda/lib/* /usr/lib
   26  snakemake --version

## Install docker
   27  sudo apt update

   30  sudo apt-get install -y apt-transport-https ca-certificates curl gnupg-agent software-properties-common
   31  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   32  sudo add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
   33  sudo apt update
   34  apt install -y docker-ce docker-ce-cli containerd.io
## test docker
   35  docker run hello-world
   36  cd foss2020/
   37  ls
   38  history >> README.md 
