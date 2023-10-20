## Fork and Clone workflows with BrokeBros

### Steps  
#### 1- Fork bros project in our Github  
#### 2- git clone <self-repo-url>  
#### 3- git remote add upstream <bros-repo-url>  
#### 4- git pull upstream main (for adding upstraem remote tracking branch)  
#### 5- git push origin main (when origin/main branch is behind main branch)  
`Note: if you want to make changes or add a new features or resolve a issue always work on feature branch`  
#### 6- git switch -c <feature-branch>    
#### 7- DO SOME WORK/CHANGES    
#### 8- git commit -a -m ""   
#### 9- git push origin <feature-branch>    
#### 10- MAKE PR FROM <self-github> <feature-branch> TO <bros-github> <main-branch>     
#### 11- IF PR GET's MERGED then it's OK:
+ if(purpose of featured branch is finished):    
  - repeat cycle from 4 to 10 for new changes/feature  
#### 12- If PR IS NOT MERGED:     
* `case-1`:feature not needed:
  - repeat cycle from 4 to 10 for new changes/feature
* `case 2`:features need more change for PR to be accepted  
  + check main branch is up to date with upstream
  + If not upto date:
    - make main up to date with upstream     
    - merge main into feature branch
  + work on that branch and repeat cycle from 7-10         	
