# git-ref
Repository used to describe git usage reference

# Change tag descripton
```
-----------------------------
-       change message      - 
-----------------------------

git tag v3.15.0 v3.15.0^{} -f -m "Penelope v3.15.0 (released onda-2)"
git push origin --delete v3.15.0
git push origin v3.15.0

git tag -d v3.15.0
```

# Renamming a tag
```
------------------------------
-        rename tag          -
------------------------------
git tag new old
git tag -d old
git push origin :refs/tags/old
git push --tags
```

# Deleting a tag
```
------------------------------
-         delete tag         -
------------------------------
# delete local tag '12345'
git tag -d 12345
# delete remote tag '12345' (eg, GitHub version too)
git push origin :refs/tags/12345
# alternative approach
git push --delete origin tagName
git tag -d tagName
```
# Deleting a local branch
```
------------------------------
-    delete branch local     -
------------------------------

git branch -d feature/login
```
# Deleting a remote branch
```
------------------------------
-    delete branch remote    -
------------------------------
git push origin --delete feature/login
```

# Seeing tags
```
------------------------------
-    git tag names           -
------------------------------
git tag -n9
```

# Seeing tags
```
------------------------------
-    git making a tag        -
------------------------------
git tag -a v3.15.0 -m "Penelope v3.15.0 (release production)"
```

# Pushing tags
```
------------------------------
-    git push remote tags    -
------------------------------
git push --tags
```

# Git alias for git-log
```
------------------------------
-    git ~/.gitconfig        -
------------------------------
[alias]
lg1 = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all
lg2 = log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold cyan)%aD%C(reset) %C(bold green)(%ar)%C(reset)%C(bold yellow)%d%C(reset)%n''          %C(white)%s%C(reset) %C(dim white)- %an%C(reset)' --all
lg = !"git lg1"
```

# Git adog
```
------------------------------
-    git log adog            -
------------------------------
[alias]
adog = log --all --decorate --oneline --graph
```
[1] - https://stackoverflow.com/questions/1057564/pretty-git-branch-graphs
