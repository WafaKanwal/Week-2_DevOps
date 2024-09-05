# Week-2_DevOps

1)Generate an SSH Key
ssh-keygen -t ed25519 -C "kanwalwafa334@gmail.com"

2)Start the SSH Agent
eval "$(ssh-agent -s)"

3)Add SSH Key to the SSH Agent
ssh-add ~/.ssh/id_ed25519

4)Copy the SSH Key to Clipboard For Windows:
cat < ~/.ssh/id_ed25519.pub

5)Add the SSH Key to GitHub
6)Go to your GitHub account settings.
7)Navigate to "SSH and GPG keys".
8)Click "New SSH key" and paste the copied key.

9)Test SSH Connection with GitHub
ssh -T git@github.com

### GIT OPERATIONS ###

1)Navigate to the Project Directory and Clone the Repository
mkdir C:/Projects
cd C:/Projects
git clone git@github.com:WafaKanwal/Week-2_DevOps.git
cd Week-2_DevOps

2)Check the Remote URL
git remote -v

3)Create a New Branch feature-x from main and Switch to It
git checkout main
git pull origin main
git checkout -b feature-x

4)Fetch the Latest Changes from main and Merge into feature-x
git fetch origin
git merge origin/main

5)Resolve Any Conflicts and Add the File for Commit
git add index.js
git commit

6)List All Branches, Including Remote Branches
git branch -a

7)Rebase feature-x onto main to Maintain a Linear History
git fetch origin
git rebase origin/main

8)Push the feature-x Branch to the Remote Repository for Review
git push origin feature-x
