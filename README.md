# Django Email Signup Example
Django signup with activation email via restful API


## Update SMTP
Please update SMTP settings (`EMAIL_*`) in `rest_email_signup/setting.py`, you can find details in [Django's document](https://docs.djangoproject.com/en/1.11/ref/settings/#std:setting-EMAIL_HOST).


## How to run
You might want to use `virtualenv` to keep the simplicity of the environment.

```
pip install -r requirements
python manage.py migrate
python manage.py runserver
```


### How to test

```
curl -H "Content-Type: application/json" -X POST -d '{"username":"yourusername","email":"youremail","password1":"secretpassword","password2":"secretpassword"}' http://localhost:8000/auth/registration/
```
