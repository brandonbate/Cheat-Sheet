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
django-admin.py startproject my_project .
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
Create an app within the project:
```
python manage.py startapp my_app
```

### Files

A basic Django project:
```
.
+--- db.sqlite3
+--- functional_tests.py
+--- geckodriver.log
+--- manage.py
+--- my_app
|    +--- admin.py
|    +--- apps.py
|    +--- __init__.py
|    +--- migrations
|    |    +--- __init__.py
|    +--- models.py
|    +--- templates
|    |    +---- home.html
|    +--- tests.py
|    +--- views.py
+--- my_project
|    +--- __init__.py
|    +--- settings.py
|    +--- urls.py
|    +--- wsgi.py
+--- virtualenv
|    +--- [...]
```

- ```functional_tests.py``` contains test code that uses Selenium and geckodriver. It can be a basic Python script (see Chapter 1) or 
use the ```unittest``` module which involves inheriting from ```unittest.TestCase``` (see Chapters 2 & 4).
- ```my_app/tests.py``` contains unit tests in a class that inherits from ```TestCase``` in ```django.test``` (see Chapter 3).
- - ```my_app/views.py``` contains function definitions that render HTML for the user.  These functions are called by ```my_project/urls.py```.
They can be can be hard code HTML (see Chapter 3) or use external HTML documents (see Chapter 4). 
- ```my_project/urls.py``` contains code that maps web addresses to rendering functions (i.e. views) in ```my_app/views.py``` (see Chapter 3).
- ```my_app/templates/home.html``` is an HTML document that can be used by ```my_app/views.py``` to serve HTML content to the user (see Chapter 4).
- ```my_project/settings.py``` contains code that registers ```my_app`` as an application within ```my_project```. This is needed for
```my_app/views.py``` to render content in ```my_app/templates/``` (see Chapter 4).




