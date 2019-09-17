# learn-git-and-github

- Git keeps asking me for my ssh key passphrase => You have to add your private key to it: ssh-add -K

- List the remote origin : git remote -v 

- Add remote url : git remote add origin "SSH address"

- Set remote url : git remote set-url origin "SSH address"

- Remove remote origin : git remote remove origin

- Git refusing to merge unrelated histories on rebase : git pull origin branchname --allow-unrelated-histories

Generating SSH key on Windows
- open git bash, create folder name .ssh, then run this : ssh-keygen.exe

