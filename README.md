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
y: copy selected | yw for word | yy for current line
"+y: for copy to clipboard
p: paste selected
ggVG: select entire file
*/#: find word in file (* forward/# backward)
d$: delete till end of line from cursor

FOLDING
za: Toggle a fold at the cursor (open if closed, close if open).
zc: Close a fold at the cursor.
zo: Open a fold at the cursor.
zC: Close all folds under the cursor recursively (closes nested folds too).
zO: Open all folds under the cursor recursively (opens nested folds too).
zj: Move cursor to the next fold.
zk: Move cursor to the previous fold.

SELECTION
v: char selection
V: line selection
w (word): Moves the cursor to the beginning of the next word, extending the selection.
e (end): Moves the cursor to the end of the current/next word, extending the selection.
b (back): Moves the cursor to the beginning of the previous word, extending the selection backward.
ge (go end): Moves the cursor to the end of the previous word, extending the

SUBSTITUTION
:s/foo/bar/: replace foo with bar on CURRENT LINE FIRST OCCURENCE
:s/foo/bar/g: replace ALL foo with bar on CURRENT LINE
:%s/foo/bar/g: replace ALL foo with bar in FILE
:%s/foo/bar/gic: replace ALL foo with bar in FILE while asking for CONFIRMATION

g (global): Replace all occurrences of the pattern on each line. If omitted, only the first occurrence on each line is replaced. 
c (confirm): Vim will prompt you for confirmation before each replacement. You'll get options like y (yes), n (no), a (all remaining), q (quit), l (last and quit). 
i (ignorecase): Perform a case-insensitive search for the pattern. 
I (matchcase): Perform a case-sensitive search. This overrides ignorecase if it's set globally.


```
