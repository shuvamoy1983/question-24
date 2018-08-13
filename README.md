# question-24

Question 24: 
To remove sensative information: 
step1)  clone the repository to your local computer.
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY

step2) cd YOUR-REPOSITORY
step3)  replacing PATH-TO-YOUR-FILE-WITH-SENSITIVE-DATA with the path to the file you want to remove
git filter-branch --force --index-filter \
'git rm --cached --ignore-unmatch PATH-TO-YOUR-FILE-WITH-SENSITIVE-DATA' \
--prune-empty --tag-name-filter cat -- --all

step 4) Add your file with sensitive data to .gitignore to ensure that you don't accidentally commit it again.
echo "YOUR-FILE-WITH-SENSITIVE-DATA" >> .gitignore
git add .gitignore
git commit -m "Add YOUR-FILE-WITH-SENSITIVE-DATA to .gitignore"

step5) 
force-push your local changes to overwrite your GitHub repository
git push origin --force --all

step 6)  To remove the sensitive file from your tagged releases,need force push against tags
git push origin --force --tags
