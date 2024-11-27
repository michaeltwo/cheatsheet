# cheatsheet
#### jupyter notebook convert to py
```
jupyter nbconvert --to script example.ipynb
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
