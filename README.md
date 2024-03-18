# PLP Git assignment steps

# Configure git in local machine
1. git config --global user-name "xx xx"
2. git config --global user.email "xxxx"
3. git config --global init.default branch main

# Remote repo set up
1. Create new repo on GitHub.com >> new repo >> name

# Local repo set up
1. Create a new folder >> mkdir PLPBasicGitAssignment 
2. Initialize a Git repo in the local folder >> git init 
3. Check status of local folder >> git status
4. Create empty README.md file >> touch README.md
5. Stage README.md file >> add README.md
6. Open README.md file on VSCode >> code .
7. Commit README.md file to remote repo >> commit -m "create Readme.md"

# Connect local and remote repo via SSH route
1. git remote add origin git@github.com:magg**/PLPBasicGitAs**
2. Configure SSH key on local machine >> ssh-keygen -t rsa -b 4096 -C *email*
3. Add SSH key to SSH agent >> ssh-add ~/.ssh/id_rsa
4. Add SSH key to GitHub account >> cat ~/.ssh/id_rsa.pub | pbcopy 
5. Verify SSH connection >> ssh -T git@github.com 
6. In case of issues, update url origin >> git remote set-url origin git@github.com:magg**/PLPBasicGitAs**
7. Double-check url of remote repo >> git remote -v

# Create file in local repo 
1. Create an empty file called hello.txt >> touch hello.txt
2. Add content to file > echo 'Hello, Git!' >hello.txt
3. Output content of file >> cat hello.txt

# Stage and commit changes to remote repo
1. Stage changes >> git add hello.txt
2. Commit changes >> git commit -m "Add hello.txt with a greeting"

# Push committed changes to remote repo
1. git push -u origin main

# Verify commits on GitHub.com
1. Visit website and confirm "hello.txt" and commit message exist