
# Starting new Python project at the centre

## Download and install Python

The instructions prepared by [Digital Ocean](https://www.digitalocean.com/community/tutorials/install-python-windows-10) have worked on 2024-10-03.

1. Download Python installer  https://www.python.org/downloads/windows/

2. If you have a second admin userID, click on ```Disable path length limit```:

  ![image](https://github.com/user-attachments/assets/c8c84fa3-1a38-45cf-b538-888f0c48a18f)

3. Add ```Python``` to the list of ```Environmental variable```

  ![image](https://github.com/user-attachments/assets/dba02098-d18d-4d8b-931e-f6cf43703a26)



## Clone from an existing GitHub repository 

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

7. Work on ```C:``` drive (network drives U and O appear to be slower)
  ```
  cd C:\Users\user.name\DSI\
  ```
