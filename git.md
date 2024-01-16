# Useful git command
1. To list committed files in git branch
```
git ls-tree --name-only -r <branch_name>
git ls-tree --name-only -r HEAD
```

2. To remove files in git but keep it in local storage
```
git rm --cached path/to/file
git rm --cached /\*.exe
```
3. To list all config
```
git config --list
git config -l
```
4. View git graph
```
git log --graph --full-history --all
git log --graph --full-history --all --pretty=format:"%h%x09%d%x20%s"
```