# Reading 32 - Permissions & Postgresql

## Permissions

**Permissions** - determine whether a request should be granted or denied access.
-run at the beginning of view.

-use `request.user` and `request.auth` authentication info to determine if incoming request should be permitted.

## How permissions are determined

*Permissions* are defined as a *list* of permission classes.
-each permission in list is examined.

**403 Forbidden** or **401 Unauthorized** if:

1.Request was authenticated but permissions denied (403 Forbidden)

2.Request was not authenticated and top authentication class doesn't use `WWW-Authenticate` headers. (403 response)

3.Same as previous but with a 401 unauthorized response.

### Object Level Permissions

-used to examine if the user is able to work on a particular object (model)

`.get_object()` - how object level permissions are run.

`exceptions.PermissionDenied` - when user is not allowed to work on object.

`.check_object_permissions(request, obj)` - method that allows one to write own views and enforce object level permissions.

```python
def get_object(self):
    obj = get_object_or_404(self.get_queryset(), pk=self.kwargs["pk"])
    self.check_object_permissions(self.request, obj)
    return obj
```

*note* - filter queryset, because generic views won't auto apply object level permissions to queryset when returning a list of objects.

### Setting Permission Policy

The default permission policy may be set globally, using the `DEFAULT_PERMISSION_CLASSES` setting.

```python
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}
```

If not specified, this setting defaults to allowing unrestricted access:

```python
'DEFAULT_PERMISSION_CLASSES': [
   'rest_framework.permissions.AllowAny',
]
```

You can also set the authentication policy on a per-view, or per-viewset basis, using the APIView class-based views.

```python
from rest_framework.permissions import IsAuthenticated
from rest_framework.response import Response
from rest_framework.views import APIView

class ExampleView(APIView):
    permission_classes = [IsAuthenticated]

    def get(self, request, format=None):
        content = {
            'status': 'request was permitted'
        }
        return Response(content)
```

Or, if you're using the @api_view decorator with function based views.

```python
from rest_framework.decorators import api_view, permission_classes
from rest_framework.permissions import IsAuthenticated
from rest_framework.response import Response

@api_view(['GET'])
@permission_classes([IsAuthenticated])
def example_view(request, format=None):
    content = {
        'status': 'request was permitted'
    }
    return Response(content)
```

### API Reference

`AllowAny` - class that allows unrestricted access and bypass authentication check.

`IsAuthenticated` - permission class that denies permission to any unauthenticated user. -Accessible to registered users.

`IsAdminUser` - permission class that will deny permission to any user unless user.is_staff is True.
-Accessible to a subset of trusted administrators.

`IsAuthenticatedOrReadOnly` - authenticated users are allowed to perform any request. Request for unauthorized users will only be permitted if request method is one of the "safe" methods (GET, HEAD, OPTIONS)

`DjangoModelPermissions` - permission class related to `django.contrib.auth` model permissions.
-applied to views that have `.queryset` property

*POST* - user must have `add` permission on model.

*PUT* and *PATCH* - user must have the `change` permission on the model.

*DELETE* - user must have `delete` permission on model.

-custom model permissions = override `DjangoModelPermissions` and set `.perms_map`.

`DjangoModelPermissionsOrAnonReadOnly` - allows unauthenticated users to have read-only access to API.

`DjangoObjectPermissions` - permission class related to object permissions framework. Add permission backend that supports object-level permissions. (django guardian)

-User permitted if they are authenticated and have *relevant per-object* and *relevant model* permissions.

*POST* - user must have `add` permission on model instance.

*PUT* and *PATCH* - user must have `change` permission on model instance.

*DELETE* - user must have `delete` permission on model instance.

### Custom Permissions

`.has_permission(self,request,view)` and `.has_object_permission(self, request, view, obj)` - return `True` if request should be granted access. (raises `PermissionDenied` if test fails)

### Overview of Access Restriction Methods

`get_queryset()` - limit general visibility of existing objects from the database.

`get_permissions` - permission examinations based on current action, request and targeted object.

`.get_serializer()` - instance level restrictions that apply to all objects on input and output.

[<==BACK](README.md)



