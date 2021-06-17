# lets the git to track all present files under root
git add .

git status
git commit -m "first commit"
# for creating branch and present on main121
git branch -M main121

# here remotely adding the url working locally
git remote add origin https://github.com/MaqOwais/DSA-py.git
## here remote means refering to github repo

# finally pushing the files to git
git push -u origin main121

