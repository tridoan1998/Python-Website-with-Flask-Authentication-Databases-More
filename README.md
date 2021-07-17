# Python-Website-with-Flask-Authentication-Databases-More

Link to youtube video tutorial: https://www.youtube.com/watch?v=dam0GPOAvVI&t=304s

We're going to also go over how you create a new user's account, how you store those in a database, how to log into those user accounts, how to log out of them, and how you associate that information with a specific user. 

Step 0( directory structure): create flask web application directory, use Visual Studio Code. Make a folder inside called website, main.py. Inside website, created static, templates, __init__.py, auth.py, models.py, views.py.
Step 1: install packags. Get Flask. pip install Flask, pip install flash-login, pip flash-splalchemy (database thing)
Step2: inside __init__.py. Set up flash application. How? Create a function create_app(). Initilize the secret key. 

Step 3: Go to main.py. grab the instance from step2. example: from website import create_app 

app = create_app()
if __name__ == '__main__':
  app.run(debug=True)

Step 4: Test run it to see the output

Creating Routes and Views:
Step 5: go to view.py. Store the standdard routes for website, where users can go to. from flask import Blueprint. Build instance Blueprint() meaning URL. Go to auth.py and do the same thing. 
@views.route('/')
def home():
  return "<h1>Test</h1>"
  
Step 6: go to __init__.py. Inside create_app(), from .views import views, do the same thing with auth 
register blueprint: app.register_blueprint(view, url_prefix='/')
Defind more routes. go to auth.py. 
#auth.route('/login')
def login():
  return "<p>login</p>"
def logout():
  return "<p>logout</p>"
def sign-up():
  return "<p>sign-up</p>"
 
Jinja templating language & HTML templates
step 7: go to templates. create new file name base.html. 
<!DOCTYPE html> #just glone the HTML and CSS code from github.
https://github.com/techwithtim/Flask-Web-App-Tutorial/tree/main/website/templates
  
