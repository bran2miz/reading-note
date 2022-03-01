# Reading 21 - Django Models

## Using Models

**models** - Python objects that django web apps access and manage data through.
-define structure of data

**multiplicities** - numbers on diagram the numbers of each model that may be present in the relationship.

### Model Primer

-models are implemented as subclasses of django.db.models.Model

```python
from django.db import models

class MyModelName(models.Model):
    """A typical class defining a model, derived from the Model class."""

    # Fields
    my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
    ...

    # Metadata
    class Meta:
        ordering = ['-my_field_name']

    # Methods
    def get_absolute_url(self):
        """Returns the url to access a particular instance of MyModelName."""
        return reverse('model-detail-view', args=[str(self.id)])

    def __str__(self):
        """String for representing the MyModelName object (in Admin site etc.)."""
        return self.my_field_name
```

-models can have any quantic number of fields.

-field type are assigned using specific classes.
-include validation records used to store and display how the field is stored or utilized.

-order that fields are declared affects default order.

### Common Field Arguments

**help_text** - text label for HTML forms

**verbose_name** - name for field used in field labels.

**default** - default value ofr the field.

**null** - default is False. If True, blank values become NULL.

**blank** - default is False; forces an input value. True = field is blank in forms.

**choices** - group of choices for field.

**primary_key** - if True, set current field as the primary key.

### Common field types

**CharField** - short to mid sized fixed-length strings.

**TextField** - large arbitrary-length strings.

**IntegerField** - field for storing integer values and validates whether entered values are integers.

**DateField** - storing/representing date/time info.

-DateField declare parameters:

1. **auto_now = True** - when saved it sets field to the current date.

2. **auto_now_add** - set date when model is created. Default = date that can be overridden by user.

**EmailField** - store and validate email

**FileField** - upload files and images respectively

**AutoField** - auto increments

**ForeignKey** - one to many relationships. One side contains the "key"; many sides contains "foreign key" of the original key.

**ManyToManyField** - specify many to many relationships.

### MetaData

**metadata** - control the default ordering of records returned when you query the model type.
-specify match order in a list of field names to ordering attribute.

```python
class Meta:
    ordering = ['-my_field_name']

    ordering = ['title', '-pubdate']
```

*note* the dash in '-pubdate' is to reverse sorting order.

### Methods

every model should define standard Python class *methods*.

*__str__()* to return strings for each object. Used to represent individual records in the administration site.

```python
def __str__(self):
    return self.field_name
```

**get_absolute_url()** - returns URL to display individual model records on the site.

```python
def get_absolute_url(self):
    """Returns the url to access a particular instance of the model."""
    return reverse('model-detail-view', args=[str(self.id)])
```

### Model Management

#### Create and Modify Records

-define model class
-define instance of the model and then call save().

```python
# Create a new record using the model's constructor.
record = MyModelName(my_field_name="Instance #1")

# Save the object into the database.
record.save()
```

#### Search Records

search using model's object attribute.

-use **objects.all** gets all records.
can grab a model in the form of a QuerySet.
-It is an iterable object, meaning that it contains a number of objects that we can iterate/loop through

```python
all_books = Book.objects.all()
```

**filter()** - filtered returned Query Set to pair text or numeric field with different validations.

```python
wild_books = Book.objects.filter(title__contains='wild')
number_wild_books = wild_books.count()
```

### Define LocalLibrary Models

**Genre model** - store into about book category.

**Book model** - info about an available book in a general sense.

## Django Admin Site

**admin app** - use models to build a site area to create, read, update, and delete records.

### SuperUser

**superuser** - full access to site but needs permission using manage.py

```python
python3 manage.py createsuperuser
```

### Logging In and Using site

1. open /admin URL and enter superuser id and password 

2. add to start creating record of that type.

3. Enter values for fields

4. Home link to go back to admin page.

5. Delete books by selecting checkbox next to unwanted book.

6. Edit by selecting name in link (same as add buttion.)

[<==BACK](README.md)
