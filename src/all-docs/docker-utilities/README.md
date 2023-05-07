# Docker Utilities

Build an image with the name trmis

```console
sudo docker build -t trmis . # . means the root directory
```

Run in Detouch mood

```console
sudo docker run --name trmis -d -p 8000:8000 trmis
```

Run without Detouch mood

```console
sudo docker run --name trmis -p 8000:8000 trmis
```

## Docker Hub

1. Create a repository in docker hub
2. Tag your image with your repo

```console
docker tag image_name repo_name(username/repo_name)
docker push repo(username/repo_name)
```

Pull and run locally

```console
docker run -p 8000:8000 mehedi182/chalawguil
```

## Docker-Django

Create superuser

```console
docker exec -it container_id python manage.py createsuperuser
```

## Docker-db

Enter DB shell

```console
sudo docker exec -it <container_id> psql -U postgres
```
