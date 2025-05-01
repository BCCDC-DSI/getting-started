# Getting Started with Python in Workbench

## Virtual environments

Creation of virtual environments allows us to build a stable, reproducible, and portable computing environment for your research projects. This strategy is applicable when you code in Python as well as R (see details from [Anaconda](https://docs.anaconda.com/free/working-with-conda/packages/using-r-language/)). For more background info, please review [Primer](https://realpython.com/python-virtual-environments-a-primer/).

Users may create multiple **virtual environments (VEs)** as project needs evolve. For instance, you may have created a VE that used R 4.1.1 last year, and wish to create a new one as you transition to R 4.3.1.

The three general steps of building VEs are:

1.  Create

2.  Activate

3.  Build, i.e. build the environment by installing (opensource) software packages

On Workbench, the following two approaches can be used to create VEs:

1.  `venv` (available as part of the standard library since Python 3.3)

    -   Choose this route for Python-only projects

2.  `miniconda` - Choose this route for projects with multiple dependencies and languages



### Via `venv`

This first approach uses Python's own `venv` module and thus frees you from the need to download and store an additional software (i.e. `miniconda`).

Now, first, decide of below options best suits your computin needs:

Option A: You may choose to place all virtual environments into a single folder where disk space is not a concern.
Option B: You may choose to create a separate VE for each each project, within each project folder  


#### Option A 

This option is more desirable if two projects require identical list of Python packages. Below are example commands to illustrate this.

Step 1: Create a new folder under your home directory 
```         
mkdir ~/my_venvs                                                 
cd ~/my_venvs                                                    
```

Step 2: Create a new virtual environment under this new folder
```
/opt/python/3.10.13/bin/python3 -m venv py310-tf         # Note -m is a switch to call the module venv        
```

Step 3: Activate the environment 
```
source ~/my_venvs/py310-tf/bin/activate   
```

Step 4: Install ``tensorflow_hub```  
```
pip install tensorflow_hub          
```

Note that suppose you were to create two Python projects under different subfolders:
- `/mnt/BCCDC/Groups/Analytics/Projects/project_A/`
- `/mnt/BCCDC/Groups/Analytics/Projects/project_B/`

Then, both can use the same virtual environment by activating once, e.g.: 
```
cd /mnt/BCCDC/Groups/Analytics/Projects/

source ~/my_venvs/py310-tf/bin/activate                                  
python project_A/process_French_texts_tf.py  # Run code for project_A 
python project_B/process_French_texts_tf.py  # Run code for project_B
```

#### Option B

This option is desirable if **none of your projects** have identical list of Python packages.

```         
cd /mnt/BCCDC/Groups/Analytics/Projects

mkdir project_X
cd project_X
/opt/python/3.10.13/bin/python3 -m venv .venv     # Step 1: Create a new virtual environment under .venv 
source .venv/bin/activate                         # Step 2: Activate
pip install tensorflow_hub                        # Step 3: Install       


mkdir project_Y
cd project_Y
/opt/python/3.10.13/bin/python3 -m venv .venv     # Step 1: Create a new virtual environment
source .venv/bin/activate                         # Step 2: Activate
pip install tensorflow_hub                        # Step 3: Install       
```

Notes: 
- If your two projects differ by few lines of code (e.g. switching from French model to an English model), Option B would require you to make two copies of identical virtual environments on your drive, which may be a problem in the long run due to limited disk space. 
- The explicit specification in the above (`/opt/python/3.10.13/bin/python3`) is required if you are new to the system and the system settings have not determined your default Python. Once the settings are done, you may simply use `python -m venv` and the default Python version will be used.

### Via `Miniconda3`


1. Download a script from Miniconda3:
    ```
    cd $HOME
    curl -sL "https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh" > "Miniconda3.sh"
    ```
2. Execute the downloaded script:
    ```
    bash Miniconda3.sh
    ```

3. Use conda to create a new VE called ```new_env```, activate, and install packages:

    ```
    conda create -c conda-forge -n new_env 
    source activate base
    conda activate new_env
    conda install numpy pandas matplotlib
    ```    

See https://educe-ubc.github.io/conda.html and [more detailed notes on VS Code](vscode.qmd)

