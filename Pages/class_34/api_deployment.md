# API Deployment

## Django Settings Best Practices

### Managing Django Settings: **Issues**

1. Different environments.
2. Sensitive data.
3. Sharing settings between team members.

> **Django settings are a Python code.** This is a curse and a blessing at the same time. It gives you _a lot of flexibility_, but can also be a problem – instead of key-value pairs, settings.py can have _a very tricky logic_.<sup>[1]</sup>

### Setting Configuration: **Different Approaches**

1. settings_local.py
    - Pros:
        - Secrets not in VCS.

    - Cons:
        - settings_local.py is not in VCS, so you can lose some of your Django environment settings.
        - The Django settings file is a Python code, so settings_local.py can have some non-obvious logic.
        - You need to have settings_local.example (in VCS) to share the default configurations for developers.
        
2. Separate settings file for each environment
    - Pros:
        - All environments are in VCS.
        - It’s easy to share settings between developers.

    - Cons:
        - You need to find a way to handle secret passwords and tokens.
        - “Inheritance” of settings can be hard to trace and maintain.


3. Environment variables
- To solve the issue with sensitive data, you can use environment variables.
- This is the simplest example using Python os.environ and it has several issues:
    I. You need to handle KeyError exceptions.
    II. You need to convert types manually (see DATABASE_PORT usage).
- To fix KeyError, you can write your own custom wrapper.

    - Pros:
        - Configuration is separated from code.
        - Environment parity – you have the same code for all environments.
        - No inheritance in settings, and cleaner and more consistent code.
        - There is a theoretical grounding for using environment variables – [12 Factors](https://djangostars.com/blog/configuring-django-settings-best-practices/#6).

    - Cons:
        - You need to handle sharing default config between developers.
        
### **12 Factors**
12 Factors is a collection of recommendations on how to build distributed web-apps that will be easy to deploy and scale in the Cloud.<sup>[1]</sup>

As the name suggests, the collection consists of twelve parts:
1. Codebase.
2. Dependencies.
3. Config.
4. Backing services.
5. Build, release, run.
6. Processes.
7. Port binding.
8. Concurrency.
9. Disposability.
10. Dev/prod parity.
11. Logs.
12. Admin processes.


### **Setting Structure**
        project/
        ├── apps/
        ├── settings/
        │   ├── __init__.py
        │   ├── djano.py
        │   ├── project.py
        │   └── third_party.py
        └── manage.py

### **Naming Conventions**
- Give meaningful names to your settings.
- Always use the prefix with the project name for your custom (project) settings.
- Write descriptions for your settings in comments.

### Django Settings: **Best practices**
- Keep settings in environment variables.
- Write default values for production configuration (excluding secret keys and tokens).
- Don’t hardcode sensitive settings, and don’t put them in VCS.
- Split settings into groups: Django, third-party, project.
- Follow naming conventions for custom (project) settings.


For more on the subject, check this **[coprehensive article](https://djangostars.com/blog/configuring-django-settings-best-practices/)** on [Django Stars](https://djangostars.com/main/)

<br/>

#

## [SSH Tutorial](https://www.hostinger.com/tutorials/ssh-tutorial-how-does-ssh-work)

#

## Things I wanna learn more about:
1. **Deployment**.
2. **Web security**.


[1]: https://djangostars.com/blog/configuring-django-settings-best-practices/