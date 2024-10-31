
# Introduction

1. Discuss with your supervisor regarding which compute environment is most sustainable
2. Email EL for account
3. Login [BCCDC's Posit workbench](https://workbench-posit.bccdc.ca/) [More screenshots](login.md)
4. Choose ```File``` > ```New``` > ```Terminal```
 
By default, Posit uses Python 3.6. To check available versions, copy-paste:
  ```
  ls -1d /opt/python/*
  ```

# Use cases 

## Scenario 1: Reproducing environment from Python Git repo (created by your peers)

### Part 1. Clone

1. Navigate to the location where you plan to save your work, e.g., create a folder called ```DSI``` in your home directory $HOME
   ```
   mkdir $HOME/DSI
   cd $HOME/DSI   
   ```
   
2. Clone the repository:
   ```
   git clone https://github.com/BCCDC-DSI/RADD.git
   ```
   
3. Optional, list the items in the repo
   ```
   cd RADD
   ls -lstr 
   ```


   
### Part 2. Build

1. Navigate to the location where your ```requirements.txt``` is saved; e.g.
   ```
   cd $HOME/DSI/RADD/workflows/part2_version2
   ```
 
2. Create a virtual environment (VE). Three options:

   Option A:
   ```
   conda create --name raddpt2 python=3.12   
   ```

   Option B: Store the VE under your folder
   ```
   mkdir $HOME/myvenv/
   conda create --prefix $HOME/myvenv/raddpt2 python=3.12  
   ```
 
   Option C: Build without use of conda
   ```
   python3 -m venv raddpt2
   ```

3. Activate virtual environment and upgrade ```pip```:

   Option A or B:
   ```
   conda activate raddpt2
   conda install pip
   ```
 
   Option C:
   ```
   source raddpt2\bin\activate
   pip install --upgrade pip
   ```


4. Build:
   ```
   pip install -r requirements.txt
   ```
   
 ![image](https://github.com/user-attachments/assets/8b6a87cc-e74c-43d5-9024-6b905604de00)




# Git

1. Configure for the first time
   ```
   git config --global user.email "you@example.com"
   git config --global user.name "your_github_username"
   ```


# Conda

Note: ```conda``` is not available by default. On 2024-10-03, we were able to download and install:

1. Download ```miniconda3``` 
  ```
  wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
  ```

2. Run the installation script:
  ```
  bash Miniconda3-latest-Linux-x86_64.sh
  ```

3. Optionally, disable the auto-initialization of conda:
  ```
  conda config --set auto_activate_base false
  ```

4. **If disabled by default**, you would need to activate conda's base environment every time you start new session:
  ```
  eval "$($HOME/miniconda3/bin/conda shell.bash hook)"
  ```

# R

## Via Launcher
![image](https://github.com/user-attachments/assets/a9e8a9f4-df82-4db0-b526-1cd93f00c486)

## Via terminal
![image](https://github.com/user-attachments/assets/ef04a109-feae-42c4-8050-fd7fe7bfb225)

## Navigating to data folders

![image](https://github.com/user-attachments/assets/28ba6067-0ed1-4819-a09e-8a6a9ef631c3)


[Return to home](..)
