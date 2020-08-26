# Django Models


 `Models` define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc.

* The definition of the model is independent of the underlying database — you can choose one of several as part of your project settings.
* Django handles all the dirty work of communicating with the database for you
* It makes sense to have separate models for every `object`
* Models are usually defined in an application's `models.py` file.

## Fields

A model can have an arbitrary number of fields, of any type — each one represents a column

Common Field Arguments

* help_text
* verbose_name
* default
* null
* blank
* choices
* primary_key

Common Field Types

* CharField
* TextField
* IntegerField
* DateField
* EmailField
* FileField
* AutoField
* ForeignKey
* ManyToManyField

## Metadata

You can declare model-level metadata for your Model by declaring class `Meta`,

> A model can also have methods.

## Registering Models

* Open Admin.py
* import models (from .models import etc)
* admin.site.register(what was imported)

You can create a superuser by running:

```t
python3 manage.py createsuperuser
```

1. To login use /admin URL
2. Click Add
3. When your finished adding click home

[Main Page](https://will-ing.github.io/reading-notes)