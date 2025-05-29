# cheatsheet

INIT FOR NEW
```
cd </path/to/my/codebase>
git init
```

INIT FOR EXISTING
```
git clone <repo>
git remote [add / set-url] origin <git@github.com:User/UserRepo.git>
git fetch --all
git branch -r       #list remote branches, remove -r for local
git checkout -b <local_branch> <remote_branch>
```

COMMIT  
```
git add .     
git commit  
or
git commit -am "commit name"
```

CREATING BRANCHES
```
local:
    git checkout -b <myFeature>
remote: [create/PUSH]
    git push origin <myFeature>
```

DELETING BRANCHES
```
git push -d <remote_name> <branchname>   # Delete remote
git branch -d <branchname>               # Delete local
```
VIM COMMANDS
```
GENERAL
gg: Go to First Line
G: Go to Last Line
y: copy selected | yw for word
"+y: for copy to clipboard
p: paste selected
ggVG: select entire file
*/#: find word in file (* forward/# backward)

FOLDING
za: Toggle a fold at the cursor (open if closed, close if open).
zc: Close a fold at the cursor.
zo: Open a fold at the cursor.
zC: Close all folds under the cursor recursively (closes nested folds too).
zO: Open all folds under the cursor recursively (opens nested folds too).
zj: Move cursor to the next fold.
zk: Move cursor to the previous fold.
```
