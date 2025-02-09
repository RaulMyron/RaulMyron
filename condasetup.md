Setting up conda non invasive

```bash
wget https://repo.anaconda.com/archive/Anaconda3-2024.02-1-Linux-x86_64.sh
#Install without auto-initialization
bash Anaconda3-2024.02-1-Linux-x86_64.sh -b -p $HOME/anaconda3
#Add minimal PATH to ~/.bashrc:
export PATH="$HOME/anaconda3/bin:$PATH"
```

```bash
code ~/.bashrc
export CONDA_NO_PLUGINS=true

# Conda control functions
function condaon() {
    source $HOME/anaconda3/etc/profile.d/conda.sh
    conda activate base
    if [[ $PS1 != *"(conda)"* ]]; then
        PS1="(conda) ${PS1}"
    fi
    echo "Conda is now ON - $(conda --version)"
}

function condaoff() {
    conda deactivate 2>/dev/null
    unset -f conda
    PS1="${PS1/\(conda\) /}"
    echo "Conda is now OFF"
}
```

Create a env and other things

```bash
# Create new environment
conda create -n project_name python=3.10

# List environments
conda env list

# Activate environment
conda activate project_name

# Deactivate environment
conda deactivate
``` 

packages management
```bash
# Install packages
conda install package_name

# List installed packages
conda list

# Export environment
conda env export > environment.yml

# Create environment from file
conda env create -f environment.yml
```
