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
###### requirements.txt
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
podman-compose down -v(del vols)
```
```
docker run -d --log-driver=json-file --log-opt max-size=10m --log-opt max-file=3 --name my-container -p 80:80 -v /path/to/html:/usr/share/nginx/html my-image
```

#### docker diagnose logs & exec $ network 
```
podman-compose logs web(web in docker-compose.yml)
```
```
podman exec -it survey_app /bin/bash
```
```
docker network ls
```
```
docker network inspect network
```
```
docker push fountain0/survey_group8:tagname
```

script files refer to scripts

## baremetal
Dell/HP
IBM

## Hypervisor
xen
esx
openstack-Linux(for VM)
OKD-fedora(for K8s nodes)

## Windows
Powershell : get-PackageSource nuget,choco,psgalley,scoop
az

## Linux
bash

## app
vMware/Citrix
k8s
k3s
minio
openstack(KVM, QEMU, Libvirt)
openshift/OKD

## Web
python
redis
postgresql
wildfly/jboss
kotlin + gradle

## commands
helm install minio minio/minio --namespace minio --set rootUser=minioadmin --set rootPassword=minio123 --set persistence.size=10Gi --set service.type=LoadBalancer
