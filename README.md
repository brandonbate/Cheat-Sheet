# Cheat Sheet

### Console Commands
Print location of current working directory:
```
pwd
```
Change current working directory:
```
cd
```
Lists files in current working directory:
```
ls
```


### venv

Create a virtual environment:
```
py -3.7 -m venv virtualenv
```
Activate a virtual environment:
```
source virtualenv/Scripts/activate
```
Deactivate a virtual environment:
```
deactivate
```

### git
Creates an empty Git repository in current working directory:
```
git init .
```
Add all content in current working directory (and subfolders) to Git staging area.
```
git add .
```
Updates git repository with latest version of files added to staging area.
```
git commit -m "message"
```
Identify tracked/untracked files. Identify whether files are unmodified, modified or staged.
```
git status
```
Adds ```file_name``` to the list of files for Git to ignore:
```
echo "file_name" >> .gitignore
git add .gitignore
git commit -m "updating .gitignore"
```
View the changes you made to the tracked files you've editted but have not yet staged:
```
git diff
```
View the difference between what you've staged and your latest commit:
```
git diff --staged
```
Remove file from system and next commit:
```
git rm my_file
```
Create a branch called ```my_branch```:
```
git branch my_branch
```
Switch to ```my_branch```:
```
git checkout my_branch
```
Merge ```my_branch``` into ```main```:
```
git checkout main
git merge my_branch
```
Delete ```my_branch```
```
git branch -d my_branch
```
Clone remote repository at ```my_url```:
```
git clone my_url
```
Connect current local machine repository to remote repository at repository_url:
```
git remote add origin repository_url
```
Update current branch with main branch of remote repository:
```
git pull
```
Update remote repository's main branch with content in current branch of local repository:
```
git push -u origin main
```

	

### Django
Creates a Django project in current directory.
```
django-admin.py startproject project_name .
```
Start the Django web server.
```
python manage.py runserver
```
Run functional tests:
```
python functional_tests.py
```
Run unit tests:
```
python manage.py test
```
	
