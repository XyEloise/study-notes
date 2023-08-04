# study-notes
personal study notes

# usage of git
click 'git bash here' at the root document,and setup a global deploy(for git to recognize the commit author):<br />
git config --global user.name "name" <br />
git config --global user.email "youremail@a.com"<br />

## set repositories
git init<br />
git add .<br />
git commit -m 'initial'<br />
git remote add origin add_ssh_address(use 'git remote -v' check,ssh can avoid login procedure,if it's http address,use 'git remote rm origin')<br />

!!!remember:if you need push/pull operation,change root to the current document<br />

## modeify repositories
git add 'new_document'/git rm --cached 'new_document'<br />
git commit -m <br />
git push origin [local beanch]:[remote branch](if error:src refsec master does not match any:repeat add . and commit opration then push)<br />

## when local repositorie different from remote:
need to update local before push:'git pull --rebase origin master'<br />

## fatal:refusing to merge unrelated histories:
'git pull origin master --allow-unrelated-histories'<br />

## two ways to push local branch to remote branch
(1)setup remote branch then pull local:<br />
git checkout -b new_remote_branch origin/new_remote_branch<br />
(2)setup local branch then push remote<br />
git checkout -b new_remote_branch (set and change to new branch)<br />
git push origin local_new_remote_branch:remote_new_remote_branch (push local new branch to remote)<br />
