# I Changed The Background
## Also uploaded it back to Github
#Darrik Puetz
I am an IT background guy with a passion for sports and cars. 
These are my biggest pet peeves. Believe this and we will be friends. 

# Growth Mindset
In my words I would say that is is the ability to learn. Don't limit yourself. You can do anything!
# Best Team In The World

## Iowa Hawkeyes
The clear choice
![Image of Yaktocat](http://www.riddell.com/media/catalog/category/Iowa_Logo.png)
http://www.riddell.com/media/catalog/category/Iowa_Logo.png
# Worst Team In The World

## Iowa State Cyclones
The worst choice
![Image of Yaktocat](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/Iowa_State_Cyclones_logo.svg/1024px-Iowa_State_Cyclones_logo.svg.png)
https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/Iowa_State_Cyclones_logo.svg/1024px-Iowa_State_Cyclones_logo.svg.png

## Useful Info
git version 2.17.1
darri$ node --version
v10.16.0
darri$ npm --version
6.9.0
darri$ eslint --version
v6.1.0
darri$ tree --version
tree v1.7.0 (c) 1996 - 2014 by Steve Baker, Thomas Moore, Francesc Rocher, Florian Sesser, Kyosuke Tokoro
darri$ echo $PSl

darri$ cat ~/.gitconfig
[user]
        email = darrikpuetz@gmail.com
        name = Darrik Puetz
[core]
        editor = nano
        
# Git

Git is a DVCS that stores data in a file system made up of snapshots. Each time you save a changed version of your project — called commit — Git creates a snapshot of the file and stores a reference to it. If the file has not changed, Git only stores a reference to the already-stored identical version of it.

## Committed
Data is securely stored in a local database

## Modified
File has been changed but not committed to the database

## Staged
Flagged a file’s changed version to be committed in the next snapshot

## Check Settings
To check settings, use the git config --list command.
## Cloning
You can also create a copy of an existing Git repository from a particular server by using the clone command with a repository’s URL:

$ git clone https://github.com/test

## Tracking and Staging a New File
Single File
Track one file only by using the following format:

git add filename
All Files
Track all files in a repository by using the following command:

$ git add *
*After using these commands, files are tracked and staged for committing.

## Committing a File
After staging one or multiple files, you should commit the changes and record what you did within the commit message:

$ git commit -m “made change x,y,z”

### Committing All Changes
$ git commit -a

## Pushing Changes
Next, you would push changes to a remote repository. We will discuss remote repositories in more depth in the next section. For now, we will look at a general overview of pushing changes to remotes.

Example:

$ git push origin master

## Seeing Your Remotes
By running the git remote command, you can view the short names, such as “origin,” of all specified remote handles.

By using git remote -v, you can view all the remote URLs next to their corresponding short names.

$ cd example
$ git remote -v
remote1 https://github.com/remote1/example (fetch)
remote1 https://github.com/remote1/example (push)
remote2 https://github.com/remote2/example (fetch)
remote2 https://github.com/remote2/example (push)
remote3 https://github.com/remote3/example (fetch)
remote3 https://github.com/remote3/example (push)
Adding Remotes
To create a new remote Git repository with a short name, use the following format:

git remote add shortname url
Example:

$ git remote
origin
$ git remote add js https://github.com/janesmith/project1
$ git remote -v
origin https://github.com/johndoe/project1 (fetch)
origin https://github.com/johndoe/project1 (push)
js     https://github.com/janesmith/project1 (fetch)
js     https://github.com/janesmith/project1 (push)
## Fetching
Fetching entails pulling data that you don’t have from a remote project.

Here is the command format:

git fetch [remote-name]

## Pushing
To push your changes “upstream” for sharing, you would use the following git push command format:

git push [remote-name][branch-name]
Example:

$ git push origin master

##  Renaming/Removing Remotes
Rename
To rename a remote’s short name, use the git remote rename command.

Example:

$ git remote rename js jane
$ git remote
origin
jane
*In the example above, we can see that the remote’s short name has been changed from js to Jane. The command git remote lists our existing remotes, which jane is now one of. The rename action also alters names of remote branches: js/master would change to jane/master.

### Remove
To remove a remote for whatever reason (e.g., a contributor has left the team, the server has moved), simply use the git remote rm command:

Example:

$ git remote rm jane
$ git remote
origin

## Commit Mistakes
You can use the –amend command when you need to alter a commit message or forgot to add some files.

$ git commit --amend
In the example above, you can use this command to easily change your commit message, if no changes were made since the newest commit.

$ git commit -m “my first commit”
$ git add example_file
$ git commit --amend

## Unstaging a File
$ git reset HEAD index.html
Unstaged changes after reset:
M index.html

## Undo a Committed Snapshot
To undo changes resulting from a particular commit, use the git revert command. This command appends a new commit that undoes changes introduced by a specific commit. This prevents Git from losing history.

$ git commit -m "Example Commit"
$ git revert HEAD

## Unmodifying a File
To have a file return to its state when you last committed, utilize the git checkout command.
Example:

$ git checkout -- index.html

## Merge 
When you want to merge changes from one branch into your current one, you can use the git merge command.

Fast-Forward Merging
With a fast-forward merge, your current branch’s pointer moves forward to the most recent commit for the branch being merged in – there is no divergent work to merge together because the latter branch is directly upstream in relation to the former one.

Example:

$ git checkout master (switches you to the master branch)
$ git merge test (merges in changes from test branch)
Updating c58d775 .. 8b9205d
Fast-forward
index.html| 4 ++
1 file changed, 4 insertions(+)

## Deleting Branches
After you’ve merged branches, and they’re no longer needed, you can easily delete them with the -d flag.

Example:

$ git branch -d test

## See Latest Commits
To see the newest commits for each branch, use the git branch-v command.

$ git branch -v
*master 51g222e updated html file
test 52c667a updated JavaScript file

## Log 
You can utilize the git log command to view committed snapshots. You can use the command to see a project’s history, use a filter, and find specific modifications. Here are example uses of the git log command:

$ git log

## Tagging
With the use of tags, Git can flag certain points in a project’s history as being significant.

To list available Git tags, use the git tag command:
Example:

git tag
 v1.0
 v2.0
 v3.0

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/darrikpuetz/darrikpuetz.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

# CSS
Selector  
 p {
 font-family: Arial;}
       Declaration
       
 h1, h2, h3 {
             Font-family: Arial;
             color: yellow;}
           (Property) (Value)

<link href="css/styles.css" type="text/css"
rel="stylesheet" />

link- where the browser will find the css
href- specific path
type- type of document being linked
rel- the relationship connection.
style- indicates style within the CSS
Selectors
        -Universal *{}
        -Type h1,h2,h3 {}
        -Class .note{}
        -ID #intoduction{}
        -Child li>a {}
        -Descendant p a {}
        -Adacent sibling h1+p {}
        -General sibling h1~p {}
#Javascript

var name = 'darik';

if (name === 'darrik') {
  //something happens here
  console.log('yeah - my name is darrik')
} else {
  console.log('sorry wrong name');
}
