# cheatsheet
#### jupyter notebook convert to py
```
jupyter nbconvert --to script example.ipynb
```
###### .env
```
DEBUG=False
SECRET_KEY='django-insecure-j9q3mm6wpn0nw1d8h-dk4u-59t1wab@+5172+hwd%8me2md))='
POSTGRES_DB=survey_group8
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
DB_HOST=db
DB_PORT=5432
```

#### git
###### .gitignore
```
.gitignore
.dockerignore
survey_group8/db_config.py
__pycache__/
.env
```

#### docker | podman
###### Build images
```
pip freeze > requirements.txt
```
###### .dockerignore
```
.dockerignore
.gitignore
.env
venv/
Dockerfile
.DS_Store
```
###### Dockfile
```
docker build --no-cache -t fountain0/survey_group8:v1 .
```
```
docker login docker.io
```
```
docker push fdeb2716ba46 docker.io/fountain0/survey_group8:latest
```
###### docker-compose.yml
```
podman-compose up --build | -d
```
```
podman-compose ps
```
```
podman-compose down
```
```
podman-compose logs web
```

#### docker log
```
docker run -d --log-driver=json-file --log-opt max-size=10m --log-opt max-file=3 --name my-container -p 80:80 -v /path/to/html:/usr/share/nginx/html my-image
```
```
docker exec -it <container_id_or_name> bash
```
```
docker network ls
```
```
docker exec -it survey_app /bin/bash
```
