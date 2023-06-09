# Reto 04

Primeramente creamos el Dockerfile tomando como imagen base apache
```
FROM httpd:2.4

LABEL project="bootcamp"

EXPOSE 80

COPY ./content/ /usr/local/apache2/htdocs
```
Creamos la imagen con el nombre ```simple-apache:new```
```
docker build . -t simple-apache:new
```
![Build de la imagen](images/build_image.png)

Podemos ver el resultado al arrancar un contenedor en ```http://localhost:5050/```
```
docker run -d --name myapache -p 5050:80 simple-apache:new
```

![Run httpd](images/run_apache.png)

## Inspeccionando la imagen

Ejecutamos el comandos ```docker inspect simple-apache:new```

![Inspect de la imagen](images/inspect_layers.png)

De igual forma, ejecutamos el comando ```docker history simple-apache:new```

![History de la imagen](images/history.png)

Podemos hacer un inspect de la imagen filtrando la sección que deseamos, en este caso vamos a filtrar la sección Layers ```docker image inspect simple-apache:new -f '{{.RootFS.Layers}}'```

![Filtro inspect](images/filtro.png)


