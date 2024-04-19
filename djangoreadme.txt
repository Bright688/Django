#create a virtual environment
#first install pip
sudo apt install pip

#upgrade pip
python3 -m pip install --user --upgrade pip

#install virtualenv
pip install virtualenv

#create virtual environment in the specified project directory by running a command.
python -m venv myenv
source myenv/bin/activate

#install django
pip3 install django

#to view django libraries in terminal use
pip freeze

To append the libraries in a requirements.txt file use:
pip freeze > requirements.txt

To install available libraries listed in the requirements.txt file, make sure your target virtual environment is active and run the following command:
pip install -r requirements.txt

#check django version 
python -m django --version

#create django project
django-admin startproject mysite

#run the django project:
python3 manage.py runserver

#create app named personal with:
django manage.py startapp personal

#add template path to the settings in TEMPLATES=[]
dir=[os.path.join(BASE_DIR, 'template')]

#Register App in settings in INSTALLED_APPS=[]
e.g INSTALLED_APPS=[
'personal',
]

#django views
e.g def home_screen(request){
  print(request.header)
  return render(request, 'base.html', {})
}

#extend all of the content in base.html to home.html
#home.html
{% extends "base.html" %}{% block title %}Home page{% endblock title %}
{%block content%}
<p>This is a homepage</p>
{%endblock%}
