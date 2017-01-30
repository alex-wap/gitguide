# Git Guide


Note: I recommend installing Homebrew if you’re using macOS. [Link](http://brew.sh/)

## Video Demo

[Git/GitHub Demo](https://youtu.be/XFJYzYeH00E)

## Initial Setup

1. Fork repo (button, top right corner) 
 	* ![Fork button](https://github.com/alex-wap/gitguide/blob/master/fork.png)
2. Clone your fork locally via the terminal: `git clone https://github.com/YOUR_USERNAME/YPC-scrum.git`
3. CD into directory `cd YPC-scrum`
4. Check existing branches `git branch -v`
5. Check the remote repos `git remote -v`. It should say: 
	* `origin https://github.com/user/repo.git (fetch)`
	* `origin https://github.com/user/repo.git (push)`
7. Add the upstream repo (original repo) in terminal:
	* `git remote add upstream https://github.com/ZakStrassberg/YPC-scrum.git`
	* If you get `fatal: remote origin already exists.`, troubleshoot [here](https://help.github.com/articles/adding-a-remote/).
	* This will be used to pull from the master branch
8. Check if the upstream was added correctly `git remote -v`


## Creating a New Feature and Saving Progress
1. **Never** work on the master branch. It is good to have one person maintain the master branch and all others working on unique branches.
2. Create a new branch for the feature you want to make (try to be descriptive and include your name) 
	* `git checkout -b alex-readme`
3. Double check the branch was made and you're on it
	* `git branch -v`
4. Once you're written some code, you can use your origin (GitHub remote repo) to save your branch's progress 
	* `git add .`
	* `git commit -m "commit message here"`
	* `git push origin alex-readme`


## Submit a Pull Request
1. Switch to your **master branch** `git checkout master`
2. **Verify that your master branch is up to date with the upstream master.** `git pull upstream master`
3. Merge your development branch into your **master branch**. `git merge alex-readme`
	* If you experience conflicts at this stage, **stop and review the conflicts**. Try `git mergetool` or download [GitKraken](https://www.gitkraken.com/).
4. Push your changes to your **GitHub master branch**. `git push origin master`
5. Go to **your** GitHub repo and select the master branch.
	* ![Branch button](https://github.com/alex-wap/gitguide/blob/master/branch.png)
6. Click the button for **New pull request** (to the right of the branch selection).
	* ![PR button](https://github.com/alex-wap/gitguide/blob/master/pr.png)
7. You will be shown two branches to compare. If it says "Able to merge" with a checkmark, you can click the create pull request button. If not, please wait to merge and discuss with your team. 
	* ![PR page](https://github.com/alex-wap/gitguide/blob/master/prpage.png)
8. There will be a textbox and a subject line with your last commit message. Update the subject line to something relevant to feature you implemented. Leave detailed comments in the textbox if there are specific things you want to let the maintainer know.
	* ![text box](https://github.com/alex-wap/gitguide/blob/master/text.png)
9. Click the Create pull request button.
	* ![Create PR](https://github.com/alex-wap/gitguide/blob/master/create.png)


## Update your Master Branch from the Remote Upstream
1. The repo maintainer should notify you when the upstream master has been updated.
2. **Save** your current work on your development branch. 
	* `git add .`
	* `git commit -m "commit message"`
	* `git push origin YOUR-BRANCH-NAME`
3. Switch to **master** branch.
	* `git checkout master`
4. Verify that the remote upstream exists and is the correct address `git remote -v`
5. Pull the changes from upstream into your master branch
	* `git pull upstream master`
6. Switch back to your development branch and continue working `git checkout YOUR-BRANCH-NAME`


