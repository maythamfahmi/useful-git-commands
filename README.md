Useful links:

 * http://ndpsoftware.com/git-cheatsheet.html
 * https://git-scm.com/doc
 * https://github.com/github/training-kit/tree/master/downloads
 * https://education.github.com/git-cheat-sheet-education.pdf
 * http://ohshitgit.com/
 * https://try.github.io/levels/1/challenges/1

#### Urls format
Github -> git@github.com:<account>/<repoName>.git
Bitbucket -> git@bitbucket.org:<account>/<repoName>.git

#### Git ignore
https://www.gitignore.io

#### Create a new repository on the command line
```
echo "# <repoName>" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:<account>/<repoName>.git
git push -u origin master
```

#### Push an existing repository from the command line
```
git remote add origin git@github.com:maythamfahmi/useful-git-commands.git
git push -u origin master
```

#### Clone repo from one server to another server including subfolders:
```
git clone --mirror GitURL
git remote add NEW-REMOTE GitURL
git push  NEW-REMOTE --mirror
```

#### Set/Change url
```
change url  -> git remote set-url origin git@bitbucket.org:maytham/mytrip.git
set new url -> git remote add origin git@bitbucket.org:maytham/mytrip.git
rem remove  -> git remote remove master
```

#### My daily push rutine for new and existing projects
create new repo in github/bitbucket
```
git clone GitURL
# start your project/copy your project files
# when done or want to push
# start with you .gitignore
git add .gitignore
git commit -m "gitignore init"
git push -u origin --all

git add .
git commit -m "basic note"
git push -u origin --all
```

#### How to git clone specific tag
```
git clone GitURL
git tag -l
git checkout tags/<tag_name>
```
or checkout and create a branch named after the revision number of tag:
```
git checkout tags/<tag_name> -b <branch_name>
```

and if you need to check tag dates

```
git log --tags --simplify-by-decoration --pretty="format:%ai %d"

```

#### Create and Checkout a New Branch
```
#branches from currently checked out directory
git checkout -b <branchName>
```

#### Checkout a Remote Branch
```
git checkout -b <localBranchName> origin/<remoteBranchName>
```

#### Abort Changes of a File
```
git checkout -- <fileName>
```

#### Modify the Previous Commit's Message
```
git commit --amend
```

#### Partial Change Checkin
```
git add --edit
```

#### Undo the Previous Commit
```
git revert HEAD^
```

#### Temporarily Stash Changes, Restore Later
```
# After changes have been made...
git stash

# Do some other stuff here, like switch branches, merge other changes, etc.

# Re-apply the changes
git stash pop
```

#### Delete a Remote Branch
```
git push origin :<branchName>
```

#### Pull in the Latest from a Shared Repository
```
# Add a remote branch
git remote add <remoteName> <gitAddress>
	# For example:  git remote add lightfaceOfficial git://github.com/darkwing/LightFace.git

# Get changes from that branch
git fetch <remoteName>
```

#### Tagging, Deleting, and Pushing Tags
```
# Create a Tag
git tag <tagName>

# Delete the tag
git tag -d <tagName>

# Push Tags
git push --tags
```

#### Who F'd it All Up?
```
git blame <fileName>
```
