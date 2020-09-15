# DRF Permissions

> Permissions in REST framework are always defined as a list of permission classes.

- The default permission policy may be set globally, using the DEFAULT_PERMISSION_CLASSES setting.
- when you set new permission classes through class attribute or decorators you're telling the view to ignore the default list set over the settings.py file.
- The AllowAny permission class will allow unrestricted access, regardless of if the request was authenticated or unauthenticated.
- The IsAdminUser permission class will deny permission to any user, unless user.is_staff
- The IsAuthenticatedOrReadOnly will allow authenticated users to perform any request. Requests for unauthorised users will only be permitted if the request method is one of the "safe" methods; GET, HEAD or OPTIONS
- o implement a custom permission, override BasePermission and implement either, or both, of the following methods:
  - .has_permission(self, request, view)
  - .has_object_permission(self, request, view, obj)


[Main Page](https://will-ing.github.io/reading-notes)