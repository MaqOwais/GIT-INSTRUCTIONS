# Below 3 commands are the adding and verifing commands 
# also these all are local effects
git add .

git status

git commit -m "first commit"

git log

# now it's time to upload into repo

## IF BRANCH IS NOT USED!

git pull origin <name of repo master branch>
## in order to get updated with repo.

git push origin <name of repo master branch>
## finally pushing away





## IF BRANCH IS USED! 
(MASTER or MAIN == REMOTE ROOT BRANCH NAME)
1. CREATE THE BRACH BOTH LOCALLY AND REMOTELY
    
    <!-- GIT BRANCH THEN BRANCH NAME (LET IT BE BRCA) -->
    git branch <branch name>
    git branch BRCA

    <!-- TO SWITCH THE BRANCHES i.e.from present(BRCA) branch to BRACH-NAME -->
    git checkout BRANCH-NAME


2. AND REMOTELY
    <!-- ORGIN IS THE NAME OF REMOTE BRANCH AND -U TELL THE GIT THAT WE WANT TO DIRECTLY MAKE LOCAL CREATED BRANCH TO REMOTE(THIS ALSO CREATES THE REMOTE BRANCH NAMED BRACH-NAME) -->
    git push -u origin BRANCH-NAME


3. THEN WE WANT THE NEWLY CREATED REMOTE BRANCH TO BE MERGED WITH MASTER OF REMOTE REPO.

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


4. FINALLY deleting the branch after merging is over

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


