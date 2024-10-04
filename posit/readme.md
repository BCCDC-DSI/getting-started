
# Introduction

1. Discuss with your supervisor regarding which compute environment is most sustainable
2. Email EL for account
3. Login [BCCDC's Posit workbench](https://workbench-posit.bccdc.ca/)
4. Choose ```File``` > ```New``` > ```Terminal```
 
By default, Posit uses Python 3.6. To check available versions, copy-paste:
  ```
  ls -1d /opt/python/*
  ```

# Use cases 

## Scenario 1: cloning Python code from existing repo (created by your peers)

1. Create virtual environment:
   ```
   conda create --name raddpt2 python=3.12  # 
   ```
 
   Or, without use of conda:
   ```
   python3 -m venv raddpt2
   ```

2. Activate virtual environment
   ```
   conda activate raddpt2
   ```
 
   Or, without use of conda:
   ```
   source raddpt2\bin\activate
   ```

3. Optionally upgrade pip:
   ```
   pip install --upgrade pip
   ```

4. Build:
   ```
   pip install -r requirementsWindows.txt
   ```
   
 ![image](https://github.com/user-attachments/assets/8b6a87cc-e74c-43d5-9024-6b905604de00)




# Git

```
git config --global user.email "you@example.com"
```

```
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

3. Disable the auto-initialization of conda:
  ```
  conda config --set auto_activate_base false
  ```

4. Activate conda's base environment:
  ```
  eval "$(/data/homes/lisa.tang/bin/ENTER/bin/conda shell.YOUR_SHELL_NAME hook)"
  ```

# R

## Via Launcher
![image](https://github.com/user-attachments/assets/a9e8a9f4-df82-4db0-b526-1cd93f00c486)

## Via terminal
![image](https://github.com/user-attachments/assets/ef04a109-feae-42c4-8050-fd7fe7bfb225)

[Return to home](..)
