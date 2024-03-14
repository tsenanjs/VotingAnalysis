# VotingAnalysis

## Setup 

1. Download all Texas legislature voting data from: https://legiscan.com/TX/datasets
2. Put files in folder called `voting_history`
3. Unzip files. Can use: 
```
import zipfile
import os
root = os.path.join(os.getcwd(),"voting_history")
folders = os.listdir(root)
for folder in folders:
    old_dir = os.path.join(root, folder)
    with zipfile.ZipFile(old_dir,"r") as zip_ref:
        new_dir = os.path.join(root, folder).replace('.zip','')
        zip_ref.extractall(new_dir)
```