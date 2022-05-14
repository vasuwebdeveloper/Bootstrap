#########Steps for creating new project##############

1) Create a folder in the directory
2) git init (Enter this command in the folder to initialize the git repo)
3) git add . (Adds all the files and folders to the repo)
4) git status ( To check the status)
5) git commit - m "Relevant commit message" (This command commits the changes to the local repoistory which is git)

6) Create a repository in the Github.
7) Clone the repository URL and connect the local repo with remote repo using below command.
  
   git remote add origin <COPIED_REPO_URL>
8) git push --set-upstream origin master 
The above command is used for two things:
1) It used to connect your local branch to remote master branch. It makes sync.
2) Deploy the local repo objects to remote repo.



>>>>>>>>>>COMMANDS<<<<<<<<<<<:

…or create a new repository on the command line

echo "# Bootstrap" >> README.md
git init
git add README.md
git add .
git commit -m "first commit"
git remote add origin https://github.com/vasuwebdeveloper/Bootstrap.git
git push --set-upstram origin master


…or push an existing repository from the command line

git remote add origin https://github.com/vasuwebdeveloper/Bootstrap.git
git branch -M main
git push -u origin main

