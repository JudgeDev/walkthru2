
**Live Coding 1**

Check existing **Python**:

python -> already got a version of python (system version)

**which** python -> /user/bin/python – system version

**pwd** -> /home/user – current directory

Install **Mambaforge**:

github.com/conda-forge/miniforge > Mambaforge linux x86 installer> copy url

(**mkdir** downloads  # new directory)

**ls**  # list directory

**cd** dowTab  # change to downloads directory with autofill

**wget** url  # download mamba

Start second terminal – don’t waste time:

Ctrl Shift 1 – new tab / Ctrl Tab – move between windows

Check for existing versions: pip uninstall ipython jupyter ¦ use which and delete directory – **rm -rf** directory  # remove, recursively, force directory

**ls -lh**  # list long form, human readable -> mambaforge.sh – shell script

**ls –help**  # lists flags

**less** mamTab  # list script

**bash** mamTab  # runs script – installs into home directory > license – yes > initializer – yes

close and reopen terminal – (base) environment

which python -> /home/user/mambaforge/bin/python – own version of python

blow away mambaforge: rm -rf mamTab, rm / Downloads/MamTab

ls -a -> .bashrc – run when terminal starts – remove conda initialize part

need to be able to reinstall easily – use script and reinstall automatically:

fastai/fastsetup > setup-conda.sh > Raw > copy url

wget url  # download script

**./**setup-conda.sh  # run script -> permission denied – downloaded files not executable

ls -l  # -rw-rw-r— - user/group/everyone – user has read and write but no execute permission  (x)

**chmod u+x**  setupTab  # add execute permission to user – rerun installer

restart terminal

Installing python libraries:

conda ¦ mamba ¦ pip – mamba is faster version of conda

ipython -> offers system install – do not use

mamba install ipython

ipython -> interactive terminal – Ctrl D to close

Install **PyTorch**:

pytorch.org/get-started/locally > Stable/Linux/Conda/Python/ > copy install command

mamba (instead of conda) command

ipython, import torch, torch.Tab (gives list of functions) – tensor(1)

torch.cuda.is\_available(), torch.cuda.device\_count(), torch.cuda.get\_device\_name(0)

Install **Jupyter**:

mamba install jupyterlab  # don’t need condaforge channel

mkdir nbs, cd nbs, jupyter lab  # starts server and opens browser or –no-browser

up arrow -> repeats command – stored in .bash\_history – create scripts from history

**Ctrl R** command – searches for command

**!!** – runs last command

**!xyz** – runs last command that starts with xyz

**Ctrl E/L** – end/beginning of line

**Alt right/left arrow** – move right/left by one word

**open .**  # open finder at this directory

**alias jl**=’jupyter lab’  # alias -> needs to go in .bashrc

Jupyter > New notebook > Save -> in nbs directory

import torch -> gives error about ipwidgets

mamba install ipwidgets

restart Juypter

**Live Coding 2**

don't normally need multiple users

**sudo -u user -I**  # switch to user in interactive terminal

**Github**:

github.com/user\_name/repository – github repository address

README.md – markdown file

Go to your github page > New repository > Name > Description > Add README > Add .gitignore – Python > License – Apache License 2.0 > Create

Edit README.md > Commit with message 




















3

