# hello-world-django
I used a Windows 10 environment command line and GitHub.com to create a "Hello World" Django application using the website URLs listed below.

https://djangoforbeginners.com/hello-world/<br>
https://docs.python.org/3/library/venv.html<br>
https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/

In the Cortana search box, type in “cmd” then click “Run as administrator”.

Navigate to your project folder by using:<br>
C:\> cd (folder name)<br>
C:\> dir/w (to list the directory contents… similar to ls in Mac/Linux terminal.<br>The /w switch causes the contents to be listed in several columns, wider, rather than in one long list.)

Windows:<br>
1.	Navigate to project folder.<br>
2.	C:\> virtualenv venv	(it seems like this command only needs to be done once per command prompt session)<br>
If this command doesn’t work, you probably need to install virtualenv by running the following command:<br>
C:\> py -m pip install –user virtualenv

If “virtualenv venv” continues to not work, try this one:

C:\> py -m venv env

3.	C:\> venv\scripts\activate	(same for this)

If you used “py -m venv env” in the previous step, use this command instead:

C:\> .\env\Scripts\activate

You should see something like this:

 

I went ahead and added a .gitignore file to my project directory that contained the following:

.DS_Store<br>
node_modules<br>
.tmp<br>
npm-debug.log<br>
wisdompets/db.sqlite3<br>
__pycache__/<br>
*.py[cod]

Here is what I have so far in my project folder:

 
The env folder that you see what automatically created by the command “py -m venv env”.<br>
Then the command “.\env\Scripts\activate” told it to use that folder.

Now, keep in mind that we will not be committing this folder to GitHub because of:

 
which it says on the website, https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/

so we will add this folder to the .gitignore file:

I think we just add a new line “env” or “env/”

.DS_Store<br>
node_modules<br>
.tmp<br>
npm-debug.log<br>
wisdompets/db.sqlite3<br>
__pycache__/<br>
*.py[cod]<br>
env

Back in the cmd window, in the virtual environment, install Django using pip:

C:\> pip install django~=3.1.0

 

C:\> cd env\scripts<br>
C:\> python.exe -m pip install –upgrade pip

 

C:\> python.exe django-admin.py startproject config D:\LinkedIn_Learning\Python\hello_world_django<br>
C:\> cd ..<br>
C:\> cd ..<br>
C:\> dir/w

 

So it looks like when I initially tried to run “django-admin startproject config .” it was trying to use a different python.exe instead of the virtual environment’s python.exe.<br>
I’ll have to look into how this is corrected later.<br>
I bet this is easier on a Mac or Linux in terminal.

C:\> python manage.py runserver

 

Then go to http://127.0.0.1:8000/ in the browser.


 

CTRL-Pause/Break causes the server to stop, and returns you to a prompt in the cmd window.

(env) C:\> git –version<br>
If this is not recognized, then you’ll probably need to go to https://git-scm.com/download/win to download Git for Windows.

After installing, you’ll need to close the cmd window and reopen it (in admin mode).<br>
Navigate again to your project folder.<br>
Activate the virtual environment:<br>
C:\> .\env\Scripts\activate<br>
C:\> git –version

 

C:\> git config –global user.name “name”<br>
C:\> git config –global user.email “email address”<br>
C:\> git init

Go to GitHub.com and create an empty repo. I’m calling mine “hello-world-django”.

C:\> git add .<br>
C:\> git commit -m “first commit”<br>
C:\> git branch -M master<br>
C:\> git remote add origin https://github.com/beebus/hello-world-django.git<br>
C:\> git push -u origin master


