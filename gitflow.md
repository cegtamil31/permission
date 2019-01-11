#Remote Git Usage

1. Signup using google account in github.
2. Create a repository as public/private(by default public).
3. Initiate README.md file.then the repository will be created.
4. It is the best practice to create new branch to work on your repo.
5. Click on the "Branch dropdown" then create the new branch in "find or create new branch text box".
6. Move to the newly created branch to create or edit your files.
7. Create new pull request to merge.
8. Merge pull request and confirm.
 
#Command line or Terminal Git Usage

#Creating the repository 
1. touch README.md
2. git init
3. git add README.md
4. git commit -m "first commit"
5. git remote add origin git@github.com:username/<reponame>.git
6. git push -u origin master

#Cloning the repository and using it.
1. "git clone <link>"
2. to create the branch:"git branch <branchname>."
3. navigate to the newly created branch:"git checkout <branchname>."
4. to create and navigate to the branch:"git checkout -b <branchname.>"
5. edit or create the files.
6. add the file to the branch:"git add <filename>."
7. commit the file:"git commit -m "message"."
8. push it to remote repo:"git push origin <branchname>."
9. checkout to master branch:"git checkout master."
10. merge the branch with master branch:"git merge master <branchname>."
1. push to remote:"git push origin master."

