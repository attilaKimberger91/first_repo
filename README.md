# first_repoc

Taks 1:

  1.
    At the home (/home/student-4322) directory I have created a couple of folders:
      $mkdir -p projects/gitIntro/first_repo
    
    Than navigated into the folder I wanted to use as a repository:
      $cd projects/gitIntro/first_repo/
      
    Now I was able to create the repository:
      $git init
      
  2.
    With nano I created file1.txt:
      $nano file1
    
    The command above created the file and opened it with nano text editor. I made my changes to the file and than pressed ctrl+x to exit.
    I was asked if i wanted to save the changes so I pressed y and than I was asked about the file name to write which had the file name I was
    working on so I pressed enter.
    
    Now the only task remained to commit the changes. First I checked the status of the repository:
      $git status

    From the status knew all the changes I made in the repository. Now I could stage the changes I made (there was only one file1):
      $git add file1
      
    And finnaly I could commit the changes:
      $git commit -m "Add file1.txt file and commit it"

  3.
    To connect to remote repository first I had to create a repository. For this I visited github.com logged into my account and created a repository.
    Than I followed the recommendation. First added the remote to my repository:
      $git remote add origin https://github.com/attilaKimberger91/first_repo
      
    Than renamed the branch to main:
      $git branch -M main
      
   4.
    To push the repository to remote server:
      $git push -u origin main
      
   5.
    To configure git to ignore files or folders first I hade to create .gitignore file. To achieve this i choose a different approach than before:
      $touch .gitignore
      
    Than I used nano to modify .gitignore:
      $nano .gitignore

    To ignore .class extension and the target folder with its contents I modified the .gitignore file the following way:    
      # ignore files with .class extension
      *.class

      # ignore target folder and its content
      target/
     
    Than I saved the changes and closed nano. Now it was ready so after I checked the status staged the changes and commited them:
      $git status
      $git add .gitignore
      $git commit -m "gitignore configuration"   -> the commit message was wrong the first when I uploaded it so later I changed it
                                                      $git rebase -i HEAD~3  
                                                        
                                                        than replaced pick with reword at the wrong commit and than pushed it using force flag:
                                                      $git push- --force origin master
                                                      
    The way I corrected my mistake might not be the best or recommended in actual project repos!
  
  6.
    To change file1 I used nano again.
      $nano file1
    
    When I finished changeing the file I saved it and exited nano. Than checked the status, staged the changes and committed them so I would be able 
    to push them to the remote repository.
      $git status
      $git add file1
      $git commit -m "Change file1.txt and send changes to the server"
      $git push

  7.
    To create a new branch named branch1:
      $git checkout -b branch1

  8.
    Again to make changes to file1 I used nano. Made the changes and saved them. Than checked the status, staged the changes and committed them.
    Finally pushed the changes to the server:
      $nano file1
      $git status
      $git add file1
      $git commit -m "In the new branch change file1.txt file and send changes to the server"
      $git push -u origin branch1

  9. 
    To merge the two branches first I checked out the main branch than merged the branches and pushed it to the remote.
      $git checkout main
      $git merge branch1
      $git push
      
  10.
    Than I deleted branch1 in the repository and the remote:
      $git branch --delete branch1
      $git push origin --delete branch1
      
    To make sure I listed the branches:
      $git branch -a
  
    
