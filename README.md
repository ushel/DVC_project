# DVC_project

git init
git add README.md
git commit -m "first commit"
git branch - M main
git remote add origin https://github.com/ushel/DVC_project.git
git push -u origin main

## Create Conda environment and activate it

conda create -n dvc-ml python=3.7 -y
conda activate dvc-ml

# if yaml if show missing install package

pip install pyyaml
pip list  -> will tell you which packages are installed.

# Install requirements file in conda environment
$ pip install -r requirements.txt  -r -> recursive installation

## Directory and file command

mkdir -p src/utils
touch src/__init__.py
touch src/utils/__init__.py

# local packages -
-e .   # will read local file setup.py and install src as package

 
# dvc commands  
dvc init

dvc repro

git rm -r --cached 'artifacts\raw_local_dir\data.csv'
git commit -m "stop tracking artifacts\raw_local_dir\data.csv"

git add dvc.lock 'artifacts\raw_local_dir\.gitignore'


if you want any stage to run always we don't add any dependencies

dvc only tracks the changes in dependencies, params... so if you want to track changes in always run you will need to add dependencies...


dvc dag

to exit pipeline press css q type css and then q