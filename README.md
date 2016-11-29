github-flow-pull-request-tutorial

This tutorial explains how and why GitHub Flow works

Step by step tutorial

1) Get a copy of the repository

by clicking fork button.

2) Clone your fork in your computer

git clone git@github.com:<your-username>/github-flow-pull-request-tutorial.git

3) Add base repository as upstream repo

git remote add upstream git@github.com:trototype/github-flow-pull-request-tutorial.git

use remote -v command to check configurations

git remote -v
origin  git@github.com:<your-username>/github-flow-pull-request-tutorial.git (fetch)
origin  git@github.com:<your-username>/github-flow-pull-request-tutorial.git (push)
upstream    git@github.com:trototype/github-flow-pull-request-tutorial.git (fetch)
upstream    git@github.com:trototype/github-flow-pull-request-tutorial.git (push)
4) Create a branch.

git checkout -b a_new_feature_name This command will create local copy of the master branch and switch your branch to new one.

5) Make your sample changes.

Add your name in WhoWasHere.md file.

6) Add, Commit & Push your changes to your fork.

git commit -m "a message for your commit"
git push origin a_new_feature_name
7) Create a Pull request for your changes in specified branch

go to your fork in github
https://github.com/<your-username>/github-flow-pull-request-tutorial
Click New pull request
Then select your a_new_feature_name branch

Compare options should be like this:
    Left side:
        base fork: trototype/github-flow-pull-re.. / base: master
    Right side:
        head fork: <your-username>/github-flow-pull-re.. / compare: a_new_feature_name

Then click 'Create pull request' button. Give a proper title for your feature. Then click the new 'Create pull request' button.
8) Discuss your pull request if necessary.

After all of these steps, base repo owners and you can comment and discuss your commits. If necessary, you can re-commit & re-push. New commits will be added to latest 'pull request' automatically.

9) Merge

Owner of upstream repository will click 'merge pull request' button, if s/he satisfied with your commits.

10) Get latest changes from base repo to your master branch.

git checkout master
git fetch upstream
git merge upsteam/master
11) Clean unnecessary branches

#delete local branch
git branch -d a_new_feature_name
#delete remote branch
git push origin --delete a_new_feature_name 
