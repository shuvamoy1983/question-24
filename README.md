# question-24

Question 24: 
To remove sensative information: 
step1)  clone the repository to your local computer.
git clone https://github.com/YOUR-USERNAME/your-repo.git

step2) cd your-repo

step3) create a new file called .gitignore with vi .gitignore and make an entry of your sensative file(as per question, the file name README.md) and save
Step4) Remove recursive the files with the below command
       git rm --cached -r .
       
Step 5) Amend the previous commit with your change: 
        git commit --amend -CHEAD
       
 Step 6) Then push it to your repository: 
         git push -f origin master      
