**Live Coding 1**

**Terminal** and **Ubuntu**:

Windows store > Windows terminal > Download > Run as administrator

wsl --install  # install windows subsystem for linux - umbuntu

Check existing **Python**:

python -> already got a version of python (system version)

**which** python -> /user/bin/python – system version

**pwd** -> /home/user – current directory

Install **Mambaforge**:

github.com/conda-forge/miniforge > Mambaforge linux x86 installer> copy url

(**mkdir** downloads  # new directory)

**ls**  # list directory

**cd** dow+Tab  # change to downloads directory with autofill

**wget** url  # download mamba

Start second terminal – don’t waste time:

Ctrl+Shift 1 – new tab / Ctrl+Tab – move between windows

Check for existing versions: pip uninstall ipython jupyter ¦ use which and delete directory – **rm -rf** directory  # remove, recursively, force directory

**ls -lh**  # list long form, human readable -> mambaforge.sh – shell script

**ls –help**  # lists flags

**less** mam+Tab  # list script

**bash** mam+Tab  # runs script – installs into home directory > license – yes > initializer – yes

close and reopen terminal – (base) environment

which python -> /home/user/mambaforge/bin/python – own version of python

blow away mambaforge: rm -rf mam+Tab, rm / Downloads/Mam+Tab

ls -a -> .bashrc – run when terminal starts – remove conda initialize part

need to be able to reinstall easily – use script and reinstall automatically:

fastai/fastsetup > setup-conda.sh > Raw > copy url

wget url  # download script

**./**setup-conda.sh  # run script -> permission denied – downloaded files not executable

ls -l  # -rw-rw-r— - user/group/everyone – user has read and write but no execute permission  (x)

**chmod u+x**  setup+Tab  # add execute permission to user – rerun installer

restart terminal

Installing python libraries:

conda ¦ mamba ¦ pip – mamba is faster version of conda

ipython -> offers system install – do not use

mamba install ipython

ipython -> interactive terminal – **Ctrl+D** to close

Install **PyTorch**:

pytorch.org/get-started/locally > Stable/Linux/Conda/Python/ > copy install command

mamba (instead of conda) command

ipython, import torch, torch.+Tab (gives list of functions) – tensor(1)

torch.cuda.is\_available(), torch.cuda.device\_count(), torch.cuda.get\_device\_name(0)

Install **Jupyter**:

mamba install jupyterlab  # don’t need condaforge channel

mkdir nbs, cd nbs, jupyter lab  # starts server and opens browser or –no-browser

up arrow -> repeats command – stored in .bash\_history – create scripts from history

**Ctrl+R** command – searches for command

**!!** – runs last command

**!xyz** – runs last command that starts with xyz

**Ctrl+E/L** – end/beginning of line

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

Github > Code > SSH > Copy ssh link

mkdir git, cd git, pwd -> /home/user/git

**git clone** ssh link -> permission denied - need ssh key

(could clone with http, but can´t push)

git config --global user.email "user", git config --global user.name "name"

or .gitconfig > email = user, name = name

**cd -**  # go back to most recently used directory

**pushd** ..., **popd**  # go back to where you pushed

**ssh keys**:

**ssh -keygen**, Enter, Enter, Enter

**cat** ~/.ssh/id_rsa.pub  # display public key, copy

Github > Profile > Settings > SSH and GPG keys > New SSH key > Title > paste key > Add SSH key

re-run git clone command -> clones into walkthru2

**tmux** - terminal multiplexer:

**sudo apt install** tmux  # system install

**tmux** -> new screen with green bar at bottom

cd git - run jupyter for where the repos are, jl

**Ctrl+B** %**  # vertical split

**Ctrl+B** ""  # horizontal split

**Ctrl+B arrow**  # move between windows

**Ctrl+B Z**  # zoom in and out

**Ctrl+B D**  # detach / tmux A  # reattch

**Juypter**:

start Jupyter - jl (might need to zoom out to get complete server address to click on)

Settings > Advanced Settings Editor (Ctrl+,) > Keyboard Shortcuts

**M** / **Y**  # Markdown / Code

Esc, **1**/**2**/**3**  # changes markdown header level

\`to be styled as code\´

**sin **Shift+Tab**  # give parameters

close with Close and Shutdown (**Ctrl+Shift+Q**) or with Tabs > x

**Git**:

**git status**  # shows notebook as untracked

**git add** notebook  # add to staging

**git commit -m** 'Add sample notebook'  # commit to local repo
**git push**  # pust to github
