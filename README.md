# DemoGit1
…or create a new repository on the command line

echo "# DemoGit" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin git@github.com:abhi1302/DemoGit.git
git push -u origin master

…or push an existing repository from the command line

git remote add origin git@github.com:abhi1302/DemoGit.git
git push -u origin master


error: src refspec master does not match any.  
error: failed to push some refs to 'ssh://xxxxx.com/project.git'



Maybe you just need to commit. I ran into this when I did:

mkdir repo && cd repo
git remote add origin /path/to/origin.git
git add .

Oops! Never committed!

git push -u origin master
error: src refspec master does not match any.

All I had to do was:

git commit -m 'initial commit'
git push origin master

Success!
