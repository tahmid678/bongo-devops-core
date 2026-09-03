# Assignment - Git & Github

## Phase 1 : The Foundations

### Task 01
- `mkdir bongo-devops-core`
- `cd bongo-devops-core`
- `git init`
- `git config --global user.name "Tahmid Jawad Annoor"`
- `git config --global user.email "tjawad98@gmail.com"`
- `touch README.md`
- `code README.md` and then edited this file.
- `git add README.md`
- `git commit` and then wrote a commit message as like the task 01.

### Task 02
- `touch .env`
- `vim .env` and `pressed i` for insert mode and then put a random password to it.
- `pressed esc` for get out of the insert mode.
- `pressed :wq` to write to the `.env` file and quit from the vim simultaneously.
- At this point, I ran `git status` and git currently tracks the `.env` file.
- `touch .gitignore`
- `vim .gitignore` and write `.env` to it.
- Now, git does not track `.env` file as `git status` shows nothing.

### Task 03
- `git checkout -b feature/system-optimization`
- `touch kernel_tuning.txt`
- `git add kernel_tuning.txt`
- `git commit`
- `git checkout main` and the file disappears.

### Task 04
- `touch web_fix.conf db_fix.conf`
- `git add web_fix.conf`
- `git commit`
- `git add db_fix.conf`
- `git commit`

### Task 05
- Created a repository in Github with the same name and copied its `ssh` url.
- In local machine, `git remote add origin <ssh>`
- `git push origin main`


## Phase 2: The Engineer's Workflow

### Task 06
- `touch port.txt` and wrote a wrong port number to it.
- `git add port.txt`
- `git commit`
- `git blame port.txt` to see who made this commit.
- `vim port.txt` and corrected the port number.
- `git add port.txt`
- `git commit`

### Task 07
- `touch main.py`
- `code main.py` and put a buggy code snippet in it.
- `git add main.py`
- `git commit`
- `touch feature.py` and add 5 lines to it.
- `git add feature.py`
- `git stash` and git hides the `feature.py` from the current branch.
- `code main.py` and fixed the buggy code snippet.
- `git add main.py`
- `git commit`
- `git stash pop` and git retrieve the `feature.py` into the current branch.

### Task 08
- `git checkout feature/system-optimization`
- Made three commits in this branch.
- `git checkout main`
- `git merge --squash feature/system-optimization` add git pull every commits from the `feature/system-optimization`, however, it does not track the changes.
- So, `git add kernel_tuning.txt`
- `git commit` and `vim` opens up with the merged commits for a new commit message.

### Task 09
- `touch optimization.txt`
- `vim optimization.txt` and add a line to it.
- `git add optimization.txt`
- `git commit`
- `git checkout -b conflict`
- `vim optimization.txt` and edit the same line.
- `git add optimization.txt`
- `git commit`
- `git checkout main`
- `vim optimization.txt` and also edit the same line here.
- `git add optimization.txt`
- `git commit`
- `git merge conflict` and it raises a conflict.
- In VSCode, I kept the both changes as a resolution.
- Later, tracked the changes before making a final commit. 