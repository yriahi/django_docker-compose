
This quick guide illustrates the usage of Docker Compose with a Django/PostgreSQL app.

## Create the following file(s):
    - Dockerfile - Defines the Django application’s image.
    - `requirements.txt` - Python dependencies file for the Django project.
    - `docker-compose.yml` - Defines the services that make your app.

Open each of the files above to explore the available settings; and adjust accordingly.

## Create an example project
`docker-compose run web django-admin.py startproject my_example_project.`
    - It creates a Django project named `my_example_project`.
    - The action takes place inside the `web` container (service) defined in `docker-compose.yml`.

## Connect Django to a PostgreSQL

Open `my_example_project/settings.py` and replace `DATABASES = ...` with

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'postgres',
        'USER': 'postgres',
        'HOST': 'db',
        'PORT': 5432,
    }
}
```

## Starting / stopping services
- Bring the containers up with `docker-compose up` or `docker-compose up -d` (background/detached mode).
- Check containers’ status by running `docker ps` or `docker-compose ps`.
- Shut down the services by typing `Ctrl-C` or `docker-compose down` (in a new shell window/tab)

