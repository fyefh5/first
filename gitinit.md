# Git initialize

1. First create the local directory  
```bash
mkdir ~/Desktop/mydir
cd ~/Desktop/mydir
git init
```
2. Then create some files
3. When done with version of your project, add them to git and commit  
```bash
git add .
git commit -m "Your message"
```
4. You can now add your repo to the remote platform such as GitHub. Just create there new repo and get its SSH address. If you have already SSH configured between your account at GitHub and your personal computer, then just run this in Git Bash:  
```bash
git remote add origin "What you copied"
git remote -v
```
5. Now you can push your commit to GitHub:  
```bash
git push -u origin main
```
