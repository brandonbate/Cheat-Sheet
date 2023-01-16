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

Creates a virtual environment:
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
Creates an empty Git repository in current working directory
```
git init .
```
Add all content in current folder (and subfolders) to Git repository.
```
git add .
```
Show which files in the current directory differ from those in the repository.
```
git status
```
Adds file_name to the list of files for Git to ignore.
```
echo "file_name" >> .gitignore
```
Tells repository to ignore files listed in .gitignore.
```
git add .gitignore
```
Updates git repository with latest version of files added:
```
git commit -m "message"
```
Add Git repository in current folder to repository created at repository_url:
```
git remote add origin repository_url
```
Push content of Git repository to the repository at the aforementioned url:
```
git push -u origin master
```
Shows differences between files in folder and those in the repository.
```
git differ
```
	

### Django
Creates a Django project in current directory.
```
django-admin.py startproject project_name .
```
Start the Django web server.
```python manage.py runserver```
	
