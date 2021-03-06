#         Django-heroku-setup


* Add this in settings.py
```python
STATIC_ROOT = os.path.join(BASE_DIR, 'static')
#or in case of error use:
STATIC_ROOT = '/statics/' 
```
#           HEROKU CLI

* [Make a Heroku account](https://signup.heroku.com/)

* [Download Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)

* [Configure Django Heroku](https://devcenter.heroku.com/articles/django-app-configuration)

* In your terminal, type in
 ```shell
git init
git add .
git commit -m "first commit"

heroku login
heroku create app_name
git push heroku master
heroku open

heroku run python manage.py migrate
```
** PS: if Heroku isn't recognized as a command, please close your terminal and editor and then re-open it.

* DEBUG = False in settings.py

* ALLOWED_HOSTS = ['your_app_name.herokuapp.com', 'localhost', '127.0.0.1'] in settings.py

* If you make edits, then just type in the terminal,
```shell
git add .
git commit -m "edit"
git push heroku master
```

