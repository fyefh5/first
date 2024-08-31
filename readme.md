# Creation of my first git

## Initialize local git repository

1. Download and install Git for Windows
2. Create a repository:  
```bash
cd ~/Desktop && mkdir first && cd first
git init
```
3. Add readme:
```bash
touch readme.md
```
4. Add it to git and then commit:
```bash
git add .
git commit -m "Add readme.md"
```

## Initialize remote git repository at GitHub

1. Check if there any ssh keys exist already:  
```bash
ls -la ~/.ssh/
```
2. Now generate the key:  
```bash
ssh-keygen -t ed25519 -C
```
3. Copy the public key:  
```bash
clip < ~/.ssh/id_ed25519.pub
```
4. Add it to your github profile
5. Check if it works:  
```bash
ssh -T git@github.com
yes
```
6. Add repo to GitHub. Just create there new 
repo and get its SSH address  
```bash
git remote add origin git@github.com:fyefh5/first.git
```
7. Check if it works:  
```bash
git remote -v
```
8. push commit:
```bash
git push -u origin main
```
9. For next pushes just use   
```bash
git bush
```

## git log

1. There are hashes that identify each commit 
uniquely  
```bash
git log
```
2. File states:

```mermaid
graph LR;
  untracked -- "git add" --> staged;
  staged    -- "git commit -m 'message_1'" --> tracked;
  tracked -- "modify this file" --> modified;
  modified -- "git add" --> staged;
  staged -- "git commit -m 'message_n'" --> tracked;
``` 

3. `git commit` commits only those files that 
are in `git add` which can be checked via  
```bash
git status
```

4. In the .git/ you can see HEAD file which 
contains the hash of the latest commit. You can 
also use HEAD instead of the latest hash.

5. `git log --oneline` shows shortened commits 
which is useful when there are too many of them

6. for oneline representation there is space for 
only 72 symbols. So, you should make message <= 
72 symbols long. Also, you should associate each 
commit with certain problem via certain style:  
- *Jira-ID*: LGS-239;
- *conventional commits*: feat, fix;
- *GitHub*: #334;
- or somehow else.


