# 3MTT_MiniProject2
Simulate Tom and Jerry scenario to illustrate collaborating on projects using Git.

## create a repo on GitHub
- repo name: 3MTT_MiniProject2 and initialize the repo with a README

## Create a working directory for Tom
```
mkdir tom
cd ~/tom/
clone git@github.com:ernynany/3MTT_MiniProject2.git
cd 3MTT_MiniProject2
``` 
![gitclone](img/tom's%20git%20clone.png)

## Create an index.html file to play with
```
<!DOCTYPE html>
<html>
<head>
    <title>Tom and Jerry Project</title>
</head>
<body>
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
        </ul>
    </nav>
    <footer>
        <p>© 2025 Tom and Jerry</p>
    </footer>
</body>
</html>
``` 

## As Tom, Add, commit, and push to origin master
```
git add index.html
git commit -m "initial HTML structure"
git push origin master
```
![commit](img/Git%20commit.png)


## create feature branch from master
```
git checkout -b update-navigation
``` 
**Tom will will add Services and Contact to the navigation panel**
```
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
	        <li><a href="#">Services</a></li> <!-- Tom added this -->
	        <li><a href="#">Contact</a></li>  <!-- Tom added this -->
        </ul>
    </nav>
```

```
git status
git add index.html
git commit -m "update to contact info"
git push origin update-navigation

``` 
## create a pull request in GitHub and merge update-navigation --> master
**As Tom, go to GitHub abd create a pull request:**
![pullrequest](img/Tom's%20pull%20request.png)

**merge the pull request:**
![pullrequest](img/merge%20the%20pull%20request.png)


![pullrequest](img/Tom's%20pull%20request2.png)

## create a working directory for Jerry
```
mkdir jerry
cd ~/jerry/
clone git@github.com:ernynany/3MTT_MiniProject2.git
cd 3MTT_MiniProject2.git

``` 
- **also create the initial HTML file for jerry after clonning the repo**
```
<!DOCTYPE html>
<html>
<head>
    <title>Tom and Jerry Project</title>
</head>
<body>
    <nav>
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
        </ul>
    </nav>
    <footer>
        <p>© 2025 Tom and Jerry</p>
    </footer>
</body>
</html>
``` 

## git pull to update the local maaster branch

```
cd
git pull origin master
``` 

## create feature branch from master
```
git checkout -b add-contact-info
``` 
**Jerry  will add some contact info to the footer**
```
    <footer>
        <p>© 2025 Tom and Jerry</p>
	    <p>Contact: doct2wise@gmail.com</p> <!-- Jerry added this -->
	    <p>Phone: 123-456-7890</p> <!-- Jerry added this -->
    </footer>
```

```
git status
git add index.html
git commit -m "added contact info to footer"
git push origin add-contact-info

``` 

## merge the branch with the master
```
git checkout master
git pull origin master
git checkout add-contact-info
git merge master
```
**Note:** This will like resolve in a merge conflict since both Tom and Jerry are working on the same index.html file. So, you have to resolve the merge conflict
- git status will show you which file the conflict is on
- manually resolve the conflict by adding or removing the wanted files.
- use vim **index.html** to edit the file
- the commit the changes and push to orign add-contact-info
![conflict](img/merge%20conflict.png)
```
git status
vim index.htnl
git add index.html
git commit -m "merge conflict from add-contact-info resolved"
git push origin add-contact-info
```

## create a pull request as Jerry to add add-contact-info --> master
- same way you created and merge Tom's pull request to the maaster, you should also be able to create and merge Jerry's pull request to the master branch.
