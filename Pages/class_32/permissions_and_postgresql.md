# Permissions & Postgresql

> Together with authentication and throttling, permissions determine whether a request should be granted or denied access. [1]

## Notes

- Permission checks are always run at the very start of the view, before any other code is allowed to proceed.
- Permission checks will typically use the authentication information in the request.user and request.auth properties to determine if the incoming request should be permitted.
- Permissions are used to grant or deny access for different classes of users to different parts of the API.
- `IsAuthenticated` class: allow access to any authenticated user, and deny access to any unauthenticated user.
- `IsAuthenticatedOrReadOnly` class: allow full access to authenticated users, but allow read-only access to unauthenticated users.


## How permissions are determined

- Permissions in REST framework are always defined as a **_list of permission classes_**.

Before running the main body of the view each permission in the list is checked. If any permission check fails, an `exceptions.PermissionDenied` or `exceptions.NotAuthenticated` exception will be raised, _and the main body of the view will not run._

- When the permission checks fail, either a "403 Forbidden" or a "401 Unauthorized" response will be returned based on [these rules](read://https_www.django-rest-framework.org/?url=https%3A%2F%2Fwww.django-rest-framework.org%2Fapi-guide%2Fpermissions%2F#how-permissions-are-determined).

## Object level permissions

Object level permissions are used to determine if a user should be allowed to act on a particular object, which **_will typically be a model instance_**.

Object level permissions are run by REST framework's **generic** views when `.get_object()` is called. As with view level permissions, an `exceptions.PermissionDenied` exception will be raised if the user is not allowed to act on the given object.

> Note: With the exception of `DjangoObjectPermissions`, the provided permission classes in `rest_framework.permissions` **do not** implement the methods necessary to check object permissions.

If you wish to use the provided permission classes in order to check object permissions, **you must** subclass them and implement the `has_object_permission()` method described in the [Custom permissions](read://https_www.django-rest-framework.org/?url=https%3A%2F%2Fwww.django-rest-framework.org%2Fapi-guide%2Fpermissions%2F#custom-permissions).


# API Reference

1. **AllowAny:**
    - The `AllowAny` permission class will allow unrestricted access, **regardless of if the request was authenticated or unauthenticated**.



2. **IsAuthenticated:**
    - The `IsAuthenticated` permission class will deny permission to any unauthenticated user, and allow permission otherwise.


3. **IsAdminUser:**
    - The `IsAdminUser` permission class will deny permission to any user, unless `user.is_staff` is `True` in which case permission will be allowed.

4. **IsAuthenticatedOrReadOnly:**
    - The `IsAuthenticatedOrReadOnly` will allow authenticated users to perform any request. Requests for unauthorised users will only be permitted if the request method is one of the "safe" methods; `GET`, `HEAD` or `OPTIONS`.

5. **DjangoModelPermissions:**
    - This permission class ties into Django's standard `django.contrib.auth` model permissions. This permission must only be applied to views that have a `.queryset` property or `get_queryset()` method. Authorization will only be granted if the user is authenticated and has the relevant model permissions assigned.

        - `POST` requests require the user to **have the `add` permission** on the model.
        - `PUT` and `PATCH` requests require the user to **have the `change` permission** on the model.
        - `DELETE` requests require the user to **have the `delete` permission** on the model.

    - The default behaviour can also be overridden to support custom model permissions. For example, you might want to include a view model permission for `GET` requests.

    - To use custom model permissions, override DjangoModelPermissions and set the .perms_map property. Refer to the source code for details.

6. **DjangoModelPermissionsOrAnonReadOnly:**
    - Similar to `DjangoModelPermissions`, but also allows unauthenticated users to have read-only access to the API.

7. **DjangoObjectPermissions:**
    - This permission class ties into Django's standard object permissions framework that allows per-object permissions on models. In order to use this permission class, you'll also need to add a permission backend that supports object-level permissions, such as django-guardian.

    - As with `DjangoModelPermissions`, this permission must only be applied to views that have a `.queryset` property or `.get_queryset()` method. Authorization will only be granted if the user is authenticated and has the relevant per-object permissions and relevant model permissions assigned.

    - DjangoObjectPermissions does not require the django-guardian package.


Form more on the subject, check this coprehensive article on [Django REST framework](www.django-rest-framework.org)



<br/>

<br/>


## **[SQL Practice](../SQL.md)**


<br/>

#

## Things I wanna learn more about:
1. SQL.
2. Querysets.








[1]: https://www.django-rest-framework.org/api-guide/permissions/
