# learn-git-and-github

- Git keeps asking me for my ssh key passphrase => You have to add your private key to it: ssh-add -K (On terminal : /usr/bin/ssh-add -K) : https://superuser.com/questions/1127067/macos-keeps-asking-my-ssh-passphrase-since-i-updated-to-sierra

- List the remote origin : git remote -v 

- Add remote url : git remote add origin "SSH address"

- Set remote url : git remote set-url origin "SSH address"

- Remove remote origin : git remote remove origin

- Git refusing to merge unrelated histories on rebase : git pull origin branchname --allow-unrelated-histories


# Remote problems (solution: use HTTPS)
- https://stackoverflow.com/questions/35558649/github-error-ssh-connect-to-host-github-com-port-22-operation-timed-out-fat
- git remote add origin-https https://github.com/alicht/tweetanuber.git
- git push -u origin-https master

# Configure git usename
```
git config --global user.name "Your Name"
git config --global user.email "youremail@yourdomain.com"
```

# Generating SSH key on Windows
- open git bash, create folder name .ssh, then run this : ssh-keygen.exe

# Generate SSH key on Mac
- https://medium.com/@pinglinh/how-to-have-2-github-accounts-on-one-machine-windows-69b5b4c5b14e
- ssh-keygen -t rsa -C “your-email-address”
- Multiple SSH keys for different GitHub accounts: https://www.cluemediator.com/multiple-ssh-keys-for-different-github-accounts

Branching
- https://stackoverflow.com/questions/42054571/making-latest-commit-master-git

GitHub Pages:
- open package.json
- add this after private=> "homepage": "https://ikhsanhabibi.github.io/robot-cards-react"
- add scripts => "predeploy": "yarn build", "deploy": "gh-pages -d build"

.gitignore
- how to make Git ignore .idea files created by Rubymine : git rm -r --cached .idea

Reset branch to the last commit
- git log
- In the server, move the cursor back to the last known good commit: git push -f origin <last_known_good_commit>:<branch_name>
- Locally, do the same: git reset (--hard) <last_known_good_commit>

Git bash on Pycharm
- Change setting in the terminal: "C:\Program Files\Git\bin\sh.exe" --login -i

- Remove all git history: https://www.willandskill.se/en/deleting-your-git-commit-history-without-removing-repo-on-github-bitbucket/
