
# Unable to checkout

```
git clone https://username:token@github.com/username/repo-name.git
Cloning into 'repo-name'...
remote: Enumerating objects: 2809, done.
remote: Counting objects: 100% (180/180), done.
remote: Compressing objects: 100% (156/156), done.
remote: Total 2809 (delta 96), reused 83 (delta 24), pack-reused 2629 (from 2)
Receiving objects: 100% (2809/2809), 178.63 MiB | 7.60 MiB/s, done.
Resolving deltas: 100% (806/806), done.
error: invalid path 'analysis_res/112shots.csv'
fatal: unable to checkout working tree
warning: Clone succeeded, but checkout failed.
You can inspect what was checked out with 'git status'
and retry with 'git restore --source=HEAD :/'
```

## Solution

```
git config --global core.protectNTFS false
```

and rerun ```git clone```


# To change the commit message

```
git commit --amend
```
