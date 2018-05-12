# Steps:
- Create the following file:
    - Dockerfile - Defines an application’s image.
    - `requirements.txt` - Python dependencies file.
    - `docker-compose.yml` -  Describes the services that make your app.

- Run command(s)
`docker-compose run web django-admin.py startproject my_example_project .`
    - This starts a django project named `my_example_project` inside the container using the `web` service.