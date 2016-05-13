#### Create remote and local repository
1. Set SSH key, backup your old ssh key(if existed).  
`$cd ~/.ssh`  
`$ssh-keygen -t rsa -C "ichenwin@gmail.com"`
2. Copy `id_rsa.pub` to Github account setting.
3. Test connection between Github.  
`$ssh -T git@github.com`
4. Create repository on Github.
5. Clone/create repository at local PC.  
`$git clone git@github.com/iChenwin/practice`  
or
```
$git init
$touch README.md
$git add README.md
$git commit -m "Init with README.md"
$git remote add origin git@github.com:iChenwin/practice.git
$git push -u origin master
```
**Notice:** the URL is `"git@github.com:iChenwin/practice.git"` not `"git@github.com/iChenwin/practice.git"` !!

Done!
#### Manage branch
1. Create local branch  
`$git checkout -b NewBranch`  
equals to  
`$git branch NewBranch`  
`$git checkout NewBranch`
2. Create branch on Github  
`$git push origin NewBranch`
3. Delete local branch  
`$git branch -d NewBranch`
4. **Delete branch on Github**  
`$git push origin --delete NewBranch`  
or  
`$git push origin :NewBranch`
5. Switch to master branch  
`$git checkout master`
6. Merge NewBranch to master.  
`git merge NewBranch`
