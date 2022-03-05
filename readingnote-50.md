# Reading 22 - Django CRUD and Forms

## Django Forms

**HTML Form** - group of one or more fields on webpage.
-grab information from users for submission to a server.

```html
<form>...</form>
```

and contain at least one input element of type = 'submit'.

**type** - attribute that defines the displayed widget.

**name and id** - field identification

**value** - attribute that defines initial value for field when first displayed.

**label** - tag that can contain a for field with id value.

**submit** - input that will be in the form of a button.

Form attribute define HTTP method used to send data and destination of that data.

**action** - URL where data is being sent to process once the form is submitted.
-not set = form submitted back to the current page URL.

**method** - HTTP method used to send the data: *POST* or *GET*

**POST** - method that is utilized if data is going to result in a change to the server's database.

**GET** - method that is utilized for forms that don't change user data.

### Django form handling process

1. View get request

2. Perform actions required including reading data from models.

**Django Form Handling**

1.Display default form when it's first requested by the user.

2.Receives data from *submit* request and ties it to the form.

3.Clean and validate the data

4.Re-display the form when data is invalid
-user populated values and error messages.

4.Perform actions when data is valid.

5.Perform actions when data is valid.

6.Direct the user to another page when actions are all complete.

**Form class** - specifies fields in:

1.form
2.layout
3.display
4.widgets
5.labels
6.initial values
7.valid values
8.error messages related to invalid values.
9.pre-defined formats

**from django import forms**
-declare form's fields

#### Validation

**clean_<fieldname>()** - easy way to validate a single field

  ```python
  def clean_renewal_date(self):
    data = self.cleaned_data['renewal_date']
    #get data and return data
    #error sources the data and validates it clean.
  ```

**ValidateError** - prompts error text

### URL Configuration

```python
urlpatterns += [
    path('book/<uuid:pk>/renew/', views.renew_book_librarian, name='renew-book-librarian'),
]
```

url configuration redirects URLs with "/catalog/book/<bookinstance_id>/renew/" to the function renew_book_librarian in views.py.

BookInstance id is now parameter *pk*.

### View

View has to comprehend whether to render the default form the first time, or a repeat call to validate data.

**POST** to submit information to the server:

1. Test against POST --> (if request.method == 'POST')
-identify form validation requests

2. GET(else)
-identify initial form creation request.

```python
import datetime

from django.shortcuts import render, get_object_or_404
from django.http import HttpResponseRedirect
from django.urls import reverse

from catalog.forms import RenewBookForm

def renew_book_librarian(request, pk):
    book_instance = get_object_or_404(BookInstance, pk=pk)

    # If this is a POST request then process the Form data
    if request.method == 'POST':

        # Create a form instance and populate it with data from the request (binding):
        form = RenewBookForm(request.POST)

        # Check if the form is valid:
        if form.is_valid():
            # process the data in form.cleaned_data as required (here we just write it to the model due_back field)
            book_instance.due_back = form.cleaned_data['renewal_date']
            book_instance.save()

            # redirect to a new URL:
            return HttpResponseRedirect(reverse('all-borrowed') )

    # If this is a GET (or any other method) create the default form.
    else:
        proposed_renewal_date = datetime.date.today() + datetime.timedelta(weeks=3)
        form = RenewBookForm(initial={'renewal_date': proposed_renewal_date})

    context = {
        'form': form,
        'book_instance': book_instance,
    }

    return render(request, 'catalog/book_renew_librarian.html', context)
```

**get_object_or_404()** - returns a specified object from a model based on primary key value.
-404 exception if record doesn't exist

**HttpResponseRedirect()** - create redirect to specified URL.

**reverse()** - generate URL from a URL config name and set of arguments.

### Model Forms

**Model Forms** - helper class that creates the form from the model.
-same as the Form class only you now have to add **class Meta**.

### Generic Editing Views

Generic editing views are used to create pages that have functionality to create, edit, and delete.

**reverse_lazy()** - redirect after something is deleted.

[<==BACK](README.md)
