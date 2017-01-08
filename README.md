# Git Guide


Note: I recommend installing Homebrew if you’re using macOS. [Link](http://brew.sh/)


## Initial Setup
1. Fork repo (button, top right corner) 


![Fork button](https://github.com/alex-wap/gitguide/blob/master/fork.png)


2. Clone your fork locally via the terminal: `git clone https://github.com/YOUR_USERNAME/YPC-scrum.git`
3. CD into directory `cd YPC-scrum`
4. Check existing branches `git branch -v`
5. Create a new branch for the feature you’re working on (try to be descriptive and include your name) 


`git checkout -b alex-readme`


6. Check the remote repo `git remote -v`. It should say 


```bash
origin https://github.com/user/repo.git (fetch) 


origin https://github.com/user/repo.git (push)
```
7. 


Check which branch you’re on and what branches exist
git branch -v
