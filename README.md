## Full Stack Flask and React on Kubernetes
Deploy a Flask-based microservice (along with Postgres and React) to a Kubernetes cluster

### How to use
Build and run: ```docker-compose  up -d --build```


### Automated unit tests and code coverage

Convention: ```docker-compose exec <service_name> python manage.py <custom_flask_cli_function>```

- Init database schema with auth/user table: ```docker-compose exec users python manage.py recreate_db```
- Seed user table: ```docker-compose exec users python manage.py seed_db```; Seeds with user: ```admin```, e-mail: ```admin@gmail.com```
- Run unit tests: ```docker-compose exec users python manage.py test```
- Code coverage: ```docker-compose exec users python manage.py cov```
- Tear it down: ```docker-compose down``` Note: you can append ```-v``` to end of the cmd to unmount volumes


### Kubernetes Instructions
WIP: TODO


### Based on the work of, credits:
* https://mherman.org/presentations/flask-kubernetes/#1
* https://kubernetes.io/blog/2019/07/23/get-started-with-kubernetes-using-python/
