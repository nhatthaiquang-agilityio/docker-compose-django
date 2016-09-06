## Django Development With Docker Compose and Machine

#Featuring:
- Docker
- Docker Compose
- Docker Machine
- Python 3.5
- Django 1.8.4
- MySQL
- Nginx
- Redis
- gunicorn

### OS X Instructions

#Run command:
+ Start new machine:
	```
	$docker-machine create -d virtualbox dev;
	$docker-machine start dev
	```

+ Build images:
	```
	$docker-compose build
	```

+ Start services:
	```
	$docker-compose up -d
	```

+ Create migrations:
	```
	$docker-compose run web /usr/local/bin/python manage.py migrate
	```

+ Run Django App:
	```
	docker-compose run web python /srv/web/manage.py runserver 0.0.0.0:8000
	```

+ Grab IP and view in your browser:
	```
	docker-machine ip dev`
	```

+ Create database:
	```
	$docker exec -it dockercomposedjango_postgres_1 bash
	$psql djangodocker --user postgres
	```

# Reference:
+ [Django Development with Docker Compose and Machine](https://realpython.com/blog/python/django-development-with-docker-compose-and-machine/)
