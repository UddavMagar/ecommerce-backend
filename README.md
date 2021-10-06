Django Template in Docker

Git
Clone this repository
$ git clone https://github.com/UddavMagar/ecommerce-backend.git

Docker
Install docker and docker-compose in your system.

create image
$ docker build -t ecommerce/api:0.0.1 .
To run the project in docker
$ docker-compose up -d			#  Will create all necessary services
Starting db ... done
Starting web   ... done
Starting worker  ... done
To stop all running containers
$ docker-compose stop			# Will stop all running services
Stopping db ... done
Stopping web   ... done
Stopping worker  ... done

Django
Once you have created all necessary services. You may want to perform some tasks on Django server like migrations, collectstatic & createsuperuser.
Use these commands respectively.
$ docker exec -it ecommerce_api bash		# Get a shell on container

# python3 manage.py collectstatic 	# Collecting static files
# python3 manage.py migrate		# Database migrate
# python3 manage.py createsuperuser	# Creating a superuser for login.
Now you should be able to access your django server on http://localhost:8000 .