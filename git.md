### git

### How to merge branch?
```
git checkout master
$: git merge issue1234
```

### How to undo the previous commit?
```
git revert HEAD^
```

### How to reset  go least change?
```
 git reset 
 get reset --hard
 git reset --hard HEAD^  //!becareful
 git checkout file_path
```

### How to add .gitignore?
add .gitignore file e.g:
```
/doc/
/target/
/.idea/
/offer.iml
```

### How to remove uploaded ignore file/fold?
```
git rm --cached file_path
git rm -r --cached fold_path
```

### Why git push no work?
```
git gc
git push
```
