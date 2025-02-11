#### setting up git bash
- git config --global user.name "your-user-name"
- git config --global user.email "your-git-signed-up-email"
- git config --global user.password "your-git-password"



---------------------------------------------------------------------------------------------------------------
- git init                          // to initialize an empty git repo
- git status                        // shows the status of the branch (untracked & modified)
- git checkout -b <branch-name>     // for creating new branch & switching to it
- git branch <branch-name>          // just create new branch, no switching
- git checkout <branch-name>        // this switches to new branch
- git branch -M main                // to create main branch

- git stash                         // just stage or temporarily save the uncommitted changes
- git stash -u                      // stage or temporarily save all changes including the uncommitted ones
- git stash apply                   // bring those temporarily done changes to your new branch. Do this after  
                                         you switched to new branch

- git log                           // logs all the status of commits
- git revert <commit-hash>          // reverts the pushed changes, this also deletes the done changes in that branch's files
- git restore --staged filename.ext // if you want to remove some file after (git add -A) i.e. unstage
- git restore --staged .            // remove all files from the stage
- git rm --cached <file>            // to unstage

- git checkout .                    // removes changes from modified files
- git clean -df                     // removes all the items from untracked directories   


- git add <filename.ext>            // adds particular files
- git add .                         // adds all the files in that folder & its sub folder
- git add -A                        // adds all the files from it's outer directory
- git commit -m "your-message"      // commits your changes in that  branch

- git remote add origin <origin-url> // for 1st time before push when you had not cloned any repo
                                    example: git remote add origin git@github.com:FullStackNest/gallery-app.git

- git remote remove origin          // to remove the origin, if some error occurred

- git push -u origin main           // -u : upstream => 1st time push,you had not cloned git repo
- git push origin                   // use this when you are in the main branch
- git push                          // use this when you want to push changes & your branch is up in the github
- git push origin <branch-name>     // to push your new branch when it's created first
- git push --set-upstream origin <branch-name> // when your branch is new, you had cloned git repo


#### DELETING Branches 

* git branch -d <branch_name> // Safely Delete a Branch (-d). This option will only allow the branch to be deleted if its 
                            // changes are already merged into the current(main) branch. 
* git branch -D <branch-name> // Forcefull delete the branch regardless of whether its changes are merged or not

##### After running either of these commands, the specified branch will be deleted from your local Git repository. If you want to delete a remote branch, you can use the git push command with the --delete option:

* git push origin --delete <branch-name>

* git rm <filenames.ext> // removes file. Then push to the git in whichever branch you are
    example: git rm file1.txt file2.txt (-f can be uesed if forcefully)

