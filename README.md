#Django & Angular 8, Packtpub
11/21/2019, Thurs


#venv3
cd /home/hal/Documents/softwares/pycharm/workspace/django/flightscheduler; source ~/venv3/bin/activate

#notes
docker-compose up --build
docker-compose up -d database 
docker-compose logs database 
docker-compose build web 
docker-compose up -d web 
docker-compose logs -f web 
docker-compose exec web python manage.py makemigrations books
docker-compose exec web python manage.py sqlmigrate books 0001 
docker-compose exec web python manage.py migrate
docker-compose run --rm database psql -U tom -h database
		password: tom
docker-compose exec web python manage.py createsuperuser
docker-compose exec web python manage.py shell
docker-compose up -d --force-recreate web  
docker-compose exec web python manage.py test
docker-compose exec web python manage.py test main.tests.test_views.TestPage.test_home_page_works
docker-compose exec web python manage.py test main.tests.test_views.TestPage
docker-compose exec web python manage.py test -v 
docker-compose exec web python manage.py showmigrations main