# django-auto-one-to-one

Automatically create child model instances when a parent class is created.

See `django_auto_one_to_one/models.py` for further documentation.

The project home page is at:

    https://chris-lamb.co.uk/projects/django-auto-one-to-one

... whilst the source and issue tracker is available at:

    https://github.com/lamby/django-auto-one-to-one



For example, given the following model definition:

```
from django.db import models
from django_auto_one_to_one import AutoOneToOneModel

class Parent(models.Model):
    field_a = models.IntegerField(default=1)

class Child(AutoOneToOneModel(Parent)):
    field_b = models.IntegerField(default=2)
```
