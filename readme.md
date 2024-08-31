# Connection via SSH

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
6. Establish remote repo binding:  
```bash
git remote add origin git@github.com:fyefh5/legion.git
```
7. Check if it works:  
```bash
git remote -v
```
8. push commit:
```bash
git push
```