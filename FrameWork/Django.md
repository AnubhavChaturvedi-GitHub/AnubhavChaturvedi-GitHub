# Django Best Guide By Anubhav Chaturvedi [YouTube Channel](https://www.youtube.com/@NetHyTech)
Django is a framework that connect the frontend and backend code (python)

## 1 install django

```
pip install django
```

## 2 Download the Django vs code extension

[Django Official Site](https://www.djangoproject.com/) || [Django Tutorial webpage](https://www.djangoproject.com/) 

## 3 Create the Django Project

```
django-admin startproject <Name Of Project>
```

## 4  To run Demo Sever Webpage

```
 python manage.py runserver
```
## 5 To create Home Urls
```
python manage.py startapp Home
```

## 6 Commang to setup for admin
```
PS C:\Users\chatu\OneDrive\Desktop\JarvisUI> python manage.py migrate       
System check identified some issues:

WARNINGS:
?: (staticfiles.W004) The directory '/var/www/static/' in the STATICFILES_DIRS setting does not exist.
Operations to perform:
  Apply all migrations: admin, auth, contenttypes, sessions
Running migrations:
  Applying contenttypes.0001_initial... OK
  Applying auth.0001_initial... OK
  Applying admin.0001_initial... OK
  Applying admin.0002_logentry_remove_auto_add... OK
  Applying admin.0003_logentry_add_action_flag_choices... OK
  Applying contenttypes.0002_remove_content_type_name... OK
  Applying auth.0002_alter_permission_name_max_length... OK
  Applying auth.0003_alter_user_email_max_length... OK
  Applying auth.0004_alter_user_username_opts... OK
  Applying auth.0005_alter_user_last_login_null... OK
  Applying auth.0006_require_contenttypes_0002... OK
  Applying auth.0007_alter_validators_add_error_messages... OK
  Applying auth.0008_alter_user_username_max_length... OK
  Applying auth.0009_alter_user_last_name_max_length... OK
  Applying auth.0010_alter_group_name_max_length... OK
  Applying auth.0011_update_proxy_permissions... OK
  Applying auth.0012_alter_user_first_name_max_length... OK
  Applying sessions.0001_initial... OK
PS C:\Users\chatu\OneDrive\Desktop\JarvisUI>
``` 
