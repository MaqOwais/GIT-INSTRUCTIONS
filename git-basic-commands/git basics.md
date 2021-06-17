
#### working area/directory --(stage fixes)--> staging area --(commit)--> git repository
####                     <---------------------------  checkout the project --|


## adding files to staging area
git add .
<!-- OR -->
git add -A


## for removing files from staging area
git reset <file name>
<!-- eg.  -->
git reset sample
<!-- to remove all files away from git staging area -->
git reset

## for commiting in local repo.
git commit -m "first commit"

### now comes the git log in order to see the committed stuff
git log


## ***** CLONING A REPO.

<!-- cloning means getting things from repo to local machine -->
git clone <url> <where to clone>
<!-- e.g. -->
git clone https://www.github.com/MaqOwais/<name of repo> <where to clone>


## after cloning viewing info about repo

<!-- this shows the location of the local machine project -->
git remote -v
<!-- this shows all the branches that are present both locally as well as remotely  -->
git branch -a


## git branch 

<!-- to get all the branches of project locally and remotely -->
git branch -a


## git diff

<!-- show the changes -->
git diff


## git pull

<!-- to pull the items present remotely as people may have added the stuff so to get sync.  -->
<!-- this is specially to make sure that everything is in sync.(i.e. no conflict b/w copies) -->

<!-- to make sure there are no conflicts and if the changes are made by another developer than that will be replicated to our local machine -->
git pull origin master


## git push

<!-- to finally push the commits we've made locally to remote repo. -->
<!-- origin here is the name of the repository and master is the branch that we like to push to -->
git push origin master


## CREATE BRANCH FOR DESIRED FEATURE

<!-- GIT BRANCH THEN BRANCH NAME (LET IT BE BRCA) -->
git branch <branch name>
git branch BRCA

<!-- TO SWITCH THE BRANCHES i.e.from present(BRCA) branch to BRACH-NAME -->
git checkout BRANCH-NAME


## NOW WE LIKE TO PUSH THE NEWLY CREATED BRANCH TO REMOTE REPO.

<!-- ORGIN IS THE NAME OF REMOTE BRANCH AND -U TELL THE GIT THAT WE WANT TO DIRECTLY MAKE LOCAL CREATED BRANCH TO REMOTE(THIS ALSO CREATES THE REMOTE BRANCH NAMED BRACH-NAME) -->
git push -u origin BRANCH-NAME


## FINALLY WE WANT THE NEWLY CREATED REMOTE BRANCH TO BE MERGED WITH MASTER OF REMOTE REPO.

<!-- here we are switching the branch to remote master -->
git checkout master

<!-- to make sure there are no conflicts and if the changes are made by another developer than that will be replicated to our local machine -->
git pull origin master

<!-- to see all the merged branches to the remote repo. and for 1st time BRANCH-NAME will not appear as it's not merged yet -->
git branch --merged

<!-- hence to merge BRANCH-NAME with master we use the below command -->
git merge BRANCH-NAME

<!-- finally we're merging this to master -->
git push origin master



## ultimately deleting the branch after merging is over

<!-- to see all the merged branches to the remote repo.  -->
<!-- since the BRANCH-NAME is already merged due to above commands here we can see the BRACH-NAME -->
<!-- just to verify -->
git branch --merged

<!-- deleting branch locally -->
git branch -d BRANCH-NAME
<!-- NOW THE BRANCH IS DELETED LOCALLY -->

<!-- to verify locally we run the command -->
git branch -a

<!-- FINALLY TO DELETE THE BRANCH REMOTELY -->
git push origin --delete BRANCH-NAME









## GOT THESE COMMANDS FROM GIT WHILE MAKING A NEW REPO (TO push an existing repository from the command line)
**git remote add origin https://github.com/MaqOwais/dsa-LB-450.git**
**git branch -M main**
**git push -u origin main**

## (TO create a new repository on the command line)

**echo "# dsa-LB-450" >> README.md**
**git init**
**git add README.md**
**git commit -m "first commit"**
**git branch -M main**
**git remote add origin https://github.com/MaqOwais/dsa-LB-450.git**
**git push -u origin main**

