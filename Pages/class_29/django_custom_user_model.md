# Django Best Practices: Custom User Model

> For a real-world project, the official Django documentation highly recommends using a custom user model instead. This provides far more flexibility down the line so, **as a general rule, always use a custom user model for all new Django projects**. [1]

## AbstractUser vs AbstractBaseUser

There are **two modern ways to create a custom user model in Django: `AbstractUser` and `AbstractBaseUser`**. In both cases we can subclass them to extend existing functionality however `AbstractBaseUser` requires much, much more work. _Seriously, don't mess with it unless you really know what you're doing_.

## Custom User Model

Creating our initial custom user model requires four steps:

1. update `django_project/settings.py`.
2. create a new `CustomUser` model.
3. create new `UserCreation` and `UserChangeForm`.
4. update the `admin`.

- **In settings.py we'll add the accounts app and use the AUTH_USER_MODEL config to tell Django to use our new custom user model in place of the built-in User model.** [1]
- **Finally we update admin.py since the Admin is highly coupled to the default User model.**
- **We can now run makemigrations and migrate for the first time to create a new database that uses the custom user model.**

### Superuser
It's helpful to create a superuser that we can use to log in to the admin and test out log in/log out.

## Templates/Views/URLs <sup>[1]</sup>

- Start by updating settings.py to use a project-level templates directory.

- Then set the redirect links for log in and log out, which will both go to our home template. Add these two lines at the bottom of the file.

        # django_project/settings.py
        LOGIN_REDIRECT_URL = "home"
        LOGOUT_REDIRECT_URL = "home"


- Create a new project-level templates folder and within it a registration folder as that's where Django will look for the log in template. We will also put our `signup.html` template in there.

- Then create four templates:

1. `base.html`
2. `home.html`
3. registration/`signup.html`
4. registration/`login.html`

- Now for our urls.py files at the project and app level.

        urlpatterns = [
            path("", TemplateView.as_view(template_name="home.html"), name="home"),
            path("admin/", admin.site.urls),
            path("accounts/", include("accounts.urls")),
            path("accounts/", include("django.contrib.auth.urls")),
        ]

- Create a `urls.py` file in the app, then fill in the following code:

        # accounts/urls.py
        from django.urls import path

        from .views import SignUpView

        urlpatterns = [
        path("signup/", SignUpView.as_view(), name="signup"),
        ]

- Last step is our views.py file in the accounts app which will contain our signup form.

        class SignUpView(CreateView):
        form_class = CustomUserCreationForm
        success_url = reverse_lazy("login")
        template_name = "registration/signup.html"

### For more in-deapth look at the steps, check this **[amazing article](https://learndjango.com/tutorials/django-custom-user-model)** by **Will Vincent** on [learndjango.com](https://learndjango.com/).



## Things I want to learn more about

**1. Forms.**

**2. Cleaning data.**

**3. Custom user model options.**

**4.  Django security.**

[1]: https://learndjango.com/tutorials/django-custom-user-model
