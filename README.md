#### Create remote and local repository
1. Set SSH key, backup your old ssh key(if existed).
```bash
$cd ~/.ssh
$ssh-keygen -t rsa -C "ichenwin@gmail.com"
```
2. Copy `id_rsa.pub` to Github account setting.
3. Test connection between Github.
```bash
$ssh -T git@github.com
```
4. Create repository on Github.
5. Clone/create repository at local PC.
```bash
$git clone git@github.com/iChenwin/practice
```
or
```bash
$git init
$touch README.md
$git add README.md
$git commit -m "Init with README.md"
$git remote add origin git@github.com:iChenwin/practice.git
$git push -u origin master
```
**Notice:** the URL is "git@github.com:iChenwin/practice.git" not "git@github.com/iChenwin/practice.git" !!

Done!
#### Manage branch
1. Create local branch
```bash
$git checkout -b NewBranch
```
equals to
```bash
$git branch NewBranch
$git checkout NewBranch
```
2. Create branch on Github
```bash
$git push origin NewBranch
```
3. Delete local branch
```bash
$git branch -d NewBranch
```
4. **Delete branch on Github**
```bash
$git push origin --delete NewBranch
```
or
```bash
$git push origin :NewBranch
```
5. Switch to master branch
```bash
$git checkout master
```
6. Merge NewBranch to master
```bash
git merge
```
