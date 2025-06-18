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
GIT RESET LOCAL
```
To revert changes made to your working copy, do this:
git restore .

To revert changes made to the index (i.e., that you have added), do this. Warning this will reset all of your unpushed commits to master!:
git reset

To revert a change that you have committed:
git revert <commit 1> <commit 2>

To remove untracked files (e.g., new files, generated files):
git clean -f

Or untracked directories (e.g., new or automatically generated directories):
git clean -fd
```
GIT STASH
```
git stash is a Git command used to temporarily save uncommitted changes in your working directory. It's a handy tool for situations where you're working on something, but need to quickly switch context to another branch or task without committing your current changes. 
Here's a breakdown of how it works and its common uses:

Saving Changes:
git stash: This saves your modified tracked files and staged changes onto a stack, clearing your working directory.
git stash push or git stash save: These commands also save your changes and can be used to add a descriptive message to the stash, making it easier to remember later. For example: git stash save "WIP: working on feature".
git stash -u or git stash --include-untracked: Includes untracked files (new files that haven't been added to Git) in the stash.
git stash -a or git stash --all: Includes both untracked and ignored files in the stash.
git stash -p or git stash --patch: Allows you to interactively choose which hunks of changes to stash.

Viewing Stashes:
git stash list: Shows a list of all your stashed changes, with identifiers like stash@{0}, stash@{1}, etc.
git stash show: Inspects the changes in the most recent stash, displaying a summary.
git stash show -p: Shows the changes of the named stash in patch form.
git stash show stash@{<index>} or git stash show <index>: Shows the changes in a specific stash.

Retrieving Stashed Changes:
git stash apply: Applies the most recent stash to your working directory but keeps it in the stash list.
git stash apply stash@{<index>} or git stash apply <index>: Applies a specific stash.
git stash pop: Applies the most recent stash and removes it from the stash list. This is generally preferred if you don't need the stash again.
git stash pop stash@{<index>}: Applies a specific stash and removes it from the stash list.

Dropping Stashes:
git stash drop: Deletes the most recent stash from the stash list.
git stash drop stash@{<index>}: Deletes a specific stash.
git stash clear: Deletes all stashes from the stash list. Use with caution as this action cannot be undone. 
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
:e filename : open a new file and edit it

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
