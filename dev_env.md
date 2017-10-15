[home](index.md)

### Dev Environment

#### Git

##### Installation & User Setup

- First check existing Git installation & location:
```
git -- version
```
```
which git
```

- Then install with Homebrew:
```
brew install git
```

- Restart the terminal & run
```
git -- version
```
```
which git
```
The latter should output: 
```
/usr/local/bin/git
```

- Set up the git user:
```
git config --global user.name "Your Name Here"
```
and
```
git config --global user.email "your_email@youremail.com"
```

##### More on the Git config file

This info will get added to your `.gitconfig` file.

- To update data at one go, the `.gitconfig` file can be edited directly. For example, github username & aliases can be set in the respective categories in the `.gitconfig` file:
```
[user]
    name = First Last
    email = email@email.com
[github]
    user = username
[alias]
    a = add
    ca = commit -a
    cam = commit -am
    s = status
    pom = push origin master
    pog = push origin gh-pages
    puom = pull origin master
    puog = pull origin gh-pages
    cob = checkout -b
[credential]
    helper = osxkeychain
```

_With the above aliases, you can run `git s` instead of `git status`._

- To push code to your GitHub repositories, use the recommended HTTPS method (versus SSH). To avoid having to type username and password everytime, enable Git password caching as described [here](https://help.github.com/articles/set-up-git/):

```
git config --global credential.helper osxkeychain
```
_(This might not work if 2FA is enabled (see [here](http://sourabhbajaj.com/mac-setup/Git/) in which case SSH is required - see below.)_

_(N.B. This can already be added by editing the `.gitconfig` file directly, as in the example before this point)_

##### Github SSH

** to add info here **

##### DS_Store

Tell git to ignore .DS_Store files (Mac-specific). To never include .DS_Store files in Git repositories, configure your Git to globally exclude those files:
Set up a `.gitignore` file to specify a global exclusion list:
```
git config --global core.excludesfile ~/.gitignore
```
```
# adding .DS_Store to that list
echo .DS_Store >> ~/.gitignore
```
