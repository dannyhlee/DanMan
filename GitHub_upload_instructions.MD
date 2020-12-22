
##### Adding Twitter API queries to Github

1. Navigate to the Github repo: https://github.com/EdwardReed1/revature_project_2
2. Click the green **Code** button.  
3. Select **SSH** and click the clipboard icon on the right side.
4. Open WSL/Linux, and navigate to the top-level directory you want the repository directory to reside underneath. 
6. Enter command:  `git clone <shift-ins>`  (this should paste the URL.  Alternatively,  CTRL-V, or right-click, or just type it out.  The format is:  git@github.com:<UserName>/<RepositoryName> .git)
7. If you receive an authentication error, its likely your SSH keys are not added to Github.  You can also enter your Github login each time, but it is much easier to add SSH keys for the long run.  Go to SSH key troubleshooting steps below.
6. With your public SSH key in hand, login into Github.com and go to to your Settings by clicking your profile icon in top right corner.
7. Click **SSH and GPG Keys** on the left hand menu column.
8. Click the green "**New SSH key**" button (top right)
9. Put a descriptive name in Title, so you remember 6 months from now which key this is.
10. Paste your key into the Key box.  Click the green "**Add SSH Key**".  You should see it listed.
11. Go back to your shell and try step 6 again.
12. If it worked, copy your Sample Data files into "revature_project_2/Sample_data/" and add any other changes you'd like to make.
13. When done making your changes, you are ready to "**add**" (move changes from working area to staging area), "**commit**"  (commit those changes, taking a snapshot of the filesystem) and "**push**" (send those changes to the remote repo on Github).
13. Enter the command: `git add . `(dot signifies your current directory recursively, so all subdirectories as well)
13. Enter the command: `git commit -m` "Some imperitive mood message" (suggested reading: https://chris.beams.io/posts/git-commit/)
14. Enter the command: `git push` (this should send your changes to Github and if you refresh you will see your changes there).  
15. Strange messages or Git conflicts?  Copy/paste them to Cliq.  We can figure them out togther, most have to do with other people making changes at the same time to the same files.

---

##### SSH key troubleshooting steps below
1. Try the command: `cat ~/.ssh/id_rsa.pub`  (your public SSH key)
2. If you see text output, type the command: `cat ~/.ssh/id_rsa.pub | clip.exe` (this copies the text to your clipboard)
3. If you do not see output, maybe you have another key name?  Try `'ls ~/.ssh/`' and scan for any <keyname>.pub files with a corresponding <keyname> file with no extension.  
4. Still no luck? Follow the instructions in Github's docs: https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
5. Bookmark that page in some subfolder, if you are like me you will look it up everytime you need to add another computer/terminal program/gitbash/virtual machine to your github account. Its nice to just type '`ssh key github`' in Chrome to have the bookmark popup.
6. Still no luck?  Could be you are not added as a contributor to the Github repo, check with Edward! 
