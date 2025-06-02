
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

1. Copy-paste API token
2. Issue following command:

  ```
  python3 -m twine upload dist/* --verbose
  ```


```
pip install -U curate-x-posts
```
