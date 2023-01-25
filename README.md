
  Step 1 :  
          # Making repository Production
          git init Production
          cd Production/
          # creating master branch
          git branch Integration
          git commit -m "Master branch created"
          # Adding a readme file
          mate README.md
          git add README.md 
          git commit -m "Master branch created"
          # Creating Integration branch
          git branch Integration
          # Creating HotFix branch
          git branch HotFix
          
Step 2 : 
          #creating Feature 1 and 2 branches that integrate to the Integration branch
          git checkout -b Feature1 Integration
          git checkout master
          git checkout -b Feature2 Integration

Step 3 : Done through github
Step 4 : git checkout Feature1
         #Making changes to feature1 using textmate editor  
         mate README.md
         git add .
         git commit -m "Made changes to feature1 " 
         git status
         #rebase with integration branch  
         git rebase --continue
         git rebase Integration
         git commit -m "remove merge conflicts"
         git rebase Integration
         git add .
         git rebase --continue
         git checkout Integration
         #merging with integration as base 
         git merge --no-ff Feature1
Step 5 : Done through github
Step 6 : git checkout Feature1
         # Making changes
         mate README.md
         #Creating pull request
         git push Production Integration
         #Merging with integration  
         git checkout Integration
         git merge --no-f Feature1
         #Merging with HotFix     
         git checkout HotFix
         git merge --no-f Feature1
         #Merging with master
         git checkout master
         git merge --no-f Feature1
Step 7 : 
         #Made changes in HotFix through github and created pull request
         git checkout Integration
         git merge --no-ff HotFix

         git checkout master
         git merge --no-ff HotFix  


     
