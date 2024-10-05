# Using Conda in Colab

1. Copy-paste into code block and run it:
    ```
    !pip install -q condacolab
    import condacolab
    condacolab.install()
    ```

2. Restart session

3. Update the ```base``` environment specified by an YML file`. For instance, suppose you clone from TextEE repo and this repo has a file ```env.yml```, then, copy-paste:
    ```
    !git clone https://github.com/ej0cl6/TextEE.git
    !conda env update -n base -f TextEE/env.yml  
    ```
   
# Using Selenium in Colab

[Colab demo](https://colab.research.google.com/drive/1MX3xY23Go1STe7LbDMvwf2KaqHpbrVhC?ouid=102659925062962217028)
- Last executed successfully on 2024-10-05
