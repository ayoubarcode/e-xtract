# e-xtract


Includes the following:

Backend:

- Django
- Django REST Framework
- JWT Authentication

Frontend:

- Next.js
- Tailwind

## Setting up the backend API

Create and activate a virtualenv:

```
$ python3 -m venv .venv
$ source .venv/bin/activate
```

Install Python requirements:

```
$ pip install -r requirements/base.txt
```

Configure the Django environment:

- Rename the sample environment file to `.env`:
    ```
    $ mv .env.sample .env
    ```
- Edit the `.env` file and provide a value for `SECRET_KEY`

Set up the DB (uses sqlite by default):

```
$ python manage.py makemigrations api
$ python manage.py migrate
```

### Running the API locally

```
$ python manage.py runserver 
```

The API is now running at http://localhost:8000

## Setting up the frontend UI

In a new shell instance, switch to the `www` folder and install JavaScript dependencies:

```
$ cd www
$ npm install
```

### Running the UI locally

```
$ npm run dev
```

The UI is now running. Visit http://localhost:3000 in your browser.

## Running tests

```
$ python manage.py test
```

