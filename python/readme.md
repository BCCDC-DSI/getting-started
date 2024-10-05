
## Using Python in external resources

- See notes on [Colab](colab)

## Starting new Python project codebase at the centre

### Download and install Python

The instructions prepared by [Digital Ocean](https://www.digitalocean.com/community/tutorials/install-python-windows-10) have worked on 2024-10-03.

1. Download [Python installer](https://www.python.org/downloads/windows/)

2. If you have a (second) admin userID, click on ```Disable path length limit```:
  ![image](https://github.com/user-attachments/assets/c8c84fa3-1a38-45cf-b538-888f0c48a18f)

3. Add ```Python``` to the list of ```Environmental variable```; here are some screenshots:
  ![image](https://github.com/user-attachments/assets/dba02098-d18d-4d8b-931e-f6cf43703a26)


### Clone from an existing GitHub repository 

To illustrate, clone from a repo containing Python code (previously prepared by your peers)

1. Work on ```C:``` drive (network drives U and O appear to be slower)
  ```
  cd C:\Users\user.name\DSI\
  ```

2. To illustrate, we will use the RADD consult as an example:
  ```
  git clone -b pt2 https://github.com/BCCDC-DSI/RADD.git
  ```

3. We'll try out the Python code under ```part2_version2```
  ```
  cd C:\Users\user.name\DSI\RADD\workflows\part2_version2\
  ```

4. Create new virtual environment named radd-p2
  ```
  python -m venv radd-p2
  ```

5. Activate it:
  ```
  radd-p2\Scripts\activate
  ```

6. Build the virtual environment by download packages specified in the ```requirementsWindows.txt```
  ```
  pip install -r requirementsWindows.txt
  ```

7. Try executing one Python script created for this project:
  ```
  python create_dataset.py
  ```


### Python in VS Code

![image](https://github.com/user-attachments/assets/9b9a4e00-eef1-481f-8529-670968911cc2)

<details>
  
<summary>Creating new notebook</summary>


1. Go to Command Palette 
  ![image](https://github.com/user-attachments/assets/692e6b67-75b6-413a-85f2-926176666e8d)

2. Search by typing "Create":
  ![image](https://github.com/user-attachments/assets/05743a5c-b868-4293-8fba-10c00dfce162)

3. Select the ```kernel```
  ![image](https://github.com/user-attachments/assets/200dd04e-9756-40b4-a8d7-eefec888d521)

</details> 


[Return to home](../)
