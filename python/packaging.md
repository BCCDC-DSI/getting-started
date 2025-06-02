
# Creating and uploading Python packages
 
## Upgrade the build package
```
python3 -m pip install --upgrade build
```

## Build the wheels
```
python3 -m build
```

Once done, the wheels will be saved under ```dist``` folder

## Upload the wheels to pypi

1. Create [PyPi account](https://pypi.org/manage/account/token/)

2. Copy-paste token:
 
  ![image](https://github.com/user-attachments/assets/89d3afcc-d2f7-4140-85a7-4534cfe1566a)

3. Issue following command:

  ```
  python3 -m twine upload dist/* --verbose
  ```


```
pip install -U curate-x-posts
```
