# Django

`Django` is a high-level Python web framework that enables rapid development of secure and maintainable websites. 

Install Django:

```t
poetry add django
```

import using

```py
import django
```

Starting a project - This will generate some default code for your initial setup

```t
django-admin startproject mysite
```

To run your server:

```t
python manage.py runserver (you can enter the port here)
```

> The path() function is passed four arguments, two required: route and view, and two optional: kwargs, and name.

```py
from django.contrib import admin
from django.urls import include, path

urlpatterns = [
    path('polls/', include('polls.urls')),
    path('admin/', admin.site.urls),
]
```


[Main Page](https://will-ing.github.io/reading-notes)