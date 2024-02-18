Cloned from: https://github.com/patrickloeber/python-github-action-template

1. Go to GitHub, create an empty repo, lets call it 'gitHubActions-pl'
    my repo: https://github.com/lesterw53679/gitHubActions-pl
2. from VSCode clone the repo from devopsjourney1 to put it on local machine
    git clone https://github.com/patrickloeber/python-github-action-template.git
3. from VSCode make any changes you want to your repo, explore the yaml file in the .github/workflows folder
4. initialize the git repo, stage the files and do a first commit (open terminal and run the following commands)
    git init
    git add .
    git commit -m "first commit"
5. check the remote connection and if needed set it to your gitHub account repo
    
    git remote get-url origin

    you will notice it is pointing to the remote repository we copied it from to our local machine
    https://github.com/patrickloeber/python-github-action-template.git

    Set the remote to your own gitHub repo
    git remote set-url origin https://github.com/lesterw53679/gitHubActions-pl

6. lets explore some other git commmands

    git branch    //this will list all the branches in your project (only main at this point)
    git branch newFeature  //this will create a new branch in your local project called 'newFeature'
    git branch    // now you will see we have two branches
    git checkout newFeature  //this will activate branch 
    git branch       //see which branch is highlighted
    git checkout main  //switch back to the main branch
    git branch -D newFeature   //delete this branch, we're not going to do anything with it right now

    (we've added a file modified it since we last staged and commit, lets do that first)
    git add .
    git commit -m "first commit"

7. Push to gitHub
    git push -u origin main    // this will push all the changes to gitHub, do another commit if you wish

8. Pull from remote  (first make some changes to the repo in GitHub, like add a readme file) 
    git pull origin main

9. Branching:  Lets try branching and doing a pull request
    git checkout -b development
 (now we are local and sitting on the "development" branch, make some modifications to files)

    git add .
    git commit -m "branch development"
    git push origin development


10. Merge Branch: Go back to GitHub and do a compare and pull, this will trigger the action because we are doing a pull and compare on this

    select the branch you want to merge into the main branch
    compare the differences, check that we have successfully passed all the tests

 11. Bring your local project up to date:
    git pull origin main    //now your local is up to date, merged branches

    if you need to delete the branch manually:
    git branch -D development

12. Note on doing matrix
on: [push, workflow_dispatch]
    branches: [main, development]
   
   branches:
      - "main"  
      - "development"


13. Install the GitHub actions extension for VSCode
    (this will make it easier to do work with actions from VSCode)
14. Break the code, raise Exception()



Links:
GitHub Docs: https://docs.github.com/en/actions
GitHub Guides: https://docs.github.com/en/actions/guides
GitHub Actions Repo: https://github.com/actions
GitHub Azure Actions Repo: https://github.com/Azure/actions

UDEMY:  Highly recommended

Maximilian Schwarzmüller (instructor) 
https://www.udemy.com/course/github-actions-the-complete-guide/#instructor-2
https://www.udemy.com/course/github-actions-the-complete-guide/


Run GitHub actions to automate a python script on a chron
Schedule Python Scripts with GitHub Actions FOR FREE | Python Automation
Patrick Loeber

https://www.youtube.com/watch?v=PaGp7Vi5gfM&t=9s

https://github.com/patrickloeber/python-github-action-template.git


Uses VSCode:
Tech With Tim GitHub: https://github.com/techwithtim
Tech With Tim GitHub Actions video: https://www.youtube.com/watch?v=UEOtZvTCmDo

TechWorld with Nana GitHub Actions CI/CD: https://www.youtube.com/watch?v=R8_veQiYBjI&t=121s


Software Engineer Tutorials: How To Use GitHub + VSCode: Create a Repository & Merge Changes With a Pull Request
https://www.youtube.com/watch?v=eLmpKKaQL54&t=363s

