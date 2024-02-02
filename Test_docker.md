Inicia sesión en [play-with-docker](https://labs.play-with-docker.com/) para acceder a tu terminal PWD.
Con copiar https://training.play-with-docker.com/beginner-linux/#Task_2

Deberás escribir tu nombre y tu contraseña, pero para ello debes estar previamente registrado en Docker.

Ahora escribe el siguiente comando en tu terminal PWD:


Vamos a crear en nuestro repositorio dos ficheros 

Primer fichero 

#### crear fichero dockerfile con  
```
 FROM nginx:latest

 COPY index.html /usr/share/nginx/html
 COPY pio.png /usr/share/nginx/html

 EXPOSE 80 443     

 CMD ["nginx", "-g", "daemon off;"]
```
#### crear fichero index.html con vuestro index
```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title> Este es mi primer sitio web con SMR </title>
  <h1>Prueba de funcionamiento contenedor docker</h1>
</head>
<body>
<h1> Mi primer sitio web con SMR</h1>
<p> Esta página está en construcción </p>
</body>
</html>
```
Ejecutar 
```
DOCKERID="TUNOMBREGIT"
```
```
echo $DOCKERID
```
#### podeis clonar el mio pero luego lo tendreis que modificar en maquina
```
git clone https://github.com/maquce69/docker-ejemplos.git
```
```
git clone "NUESTRO REPOSITORIO"
```
#### Si se ha creado en un directorio  meteros en vuestro git y revisar con un "ls" que este todo
En el path devuestro git ejecuar la composicion

#### Crear
```
docker build -t $DOCKERID/web:1.0 .
```
#### Arrancarlo

```
docker run -d -p 80:80 --name servidor_web $DOCKERID/quirosweb:0.2
```
#### Matarlo
```
docker rm --force quiros_web
```
# Prueba mario bros
```
docker run -d -p 8600:8080 pengbai/docker-supermario
```
