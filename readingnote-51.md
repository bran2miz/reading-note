# Reading 29 - Django Custom User

## Django Custom User Model

**Custom User Model** - provides more flexibility.

*note* always use a custom user model for new Django projects.

### Setup

1.Create a new directory called *accounts* for code.
2.Install Django.
3.Make new Django project called config
4.Make a new app called projects.
5.Start and run local web server.

### AbstractUser vs AbstractBaseUser

**AbstractUser** - subclasses AbstractBaseUser(because BaseUser requires ALOT of work), allowing more default configurations.

### Custom User Model

1.Update config/settings.py (add accounts app and use Custom User Model)
2.Create new CustomUserModel.
3.Create new UserCreation and UserChangeForm.
4.Update admin

*note* add accounts app into settings.py and AUTH_USER_MODEL so that it replaces the already built in User model.

```python
# config/settings.py
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'accounts', # new
]
...
AUTH_USER_MODEL = 'accounts.CustomUser' # new
```

*note* update accounts/models.py and add new custom model class.

```python
# accounts/models.py
from django.contrib.auth.models import AbstractUser
from django.db import models

class CustomUser(AbstractUser):
    pass
    # add additional fields in here

    def __str__(self):
        return self.username
```

*note* create new file in accounts called forms.py

  touch accounts/forms.py

Need new versions of two form methods that will receive heavy use working with users.

```python
# accounts/forms.py
from django import forms
from django.contrib.auth.forms import UserCreationForm, UserChangeForm
from .models import CustomUser

class CustomUserCreationForm(UserCreationForm):

    class Meta:
        model = CustomUser
        fields = ('username', 'email')

class CustomUserChangeForm(UserChangeForm):

    class Meta:
        model = CustomUser
        fields = ('username', 'email')
```

*note* update admin.py with CustomUserAdmin since Admin is highly coupled to the default User model.

```python
# accounts/admin.py
from django.contrib import admin
from django.contrib.auth.admin import UserAdmin

from .forms import CustomUserCreationForm, CustomUserChangeForm
from .models import CustomUser

class CustomUserAdmin(UserAdmin):
    add_form = CustomUserCreationForm
    form = CustomUserChangeForm
    model = CustomUser
    list_display = ['email', 'username',]

admin.site.register(CustomUser, CustomUserAdmin)
```

*note* run make migrations and migrate, which creates a new database that uses the custom user model.

### Superuser

use *superuser* to test out login/logout
  python manage.py create superuser

## DjangoX

DjangoX is a starter project created by **William Vincent**.

-comes with a custom user model by default.

-email and password authentication instead of the default that Django has provided.

-fully extendable with authentication via social media and email.

-Vincent keeps this project accessible to anyone and flexible enough to support endless possibilities for custom configuration.

## Abstract User, User Profile and Signals in Django

1.New Project

```python
from django.contrib.auth.models import AbstractUser

class User(AbstractUser):
  pass
```

in settings.py:

```python
settings.AUTH_USER_MODEL
```

2.Add User class *note* must add before migrate.
3. ./manage.py migrate

1. UserProfile (the custom user model) takes in django User as a one to one field.

2. creates post_save signal (every time user model is saved)

3. load signal into the app.

[<==BACK](README.md)
