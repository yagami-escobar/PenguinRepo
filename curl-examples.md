### Guia Flags:
```
-I | --head     -> Muestra solo la cabezera de la petición.
-v | --verbose  -> Muestra de forma más detallada la petición.
-L | --location -> Sigue las redirecciones del sitio web, es recomendable su uso.
-O | --remote-name -> Descarga el recurso con el mismo nombre del recurso remoto, no se puede setear.
-o | --output   -> Descarga el archivo permitiendo cambiar el nombre del recurso remoto.
-X | --request  -> Sirve para especificar el tipo de petición a usar(GET, POST, OPTIONS, etc)
```

### Consultar el Header del Recurso/Servicio/API/etc

***Request***
```
curl --head http://35.202.138.44/wp-admin/install.php || curl -I http://35.202.138.44/wp-admin/install.php 
```
***Output***
```
HTTP/1.1 200 OK
Date: Wed, 22 Jun 2022 21:54:16 GMT
Server: Apache/2.4.7 (Ubuntu)
X-Powered-By: PHP/5.5.9-1ubuntu4.14
Expires: Wed, 11 Jan 1984 05:00:00 GMT
Cache-Control: no-cache, must-revalidate, max-age=0
Pragma: no-cache
Content-Type: text/html; charset=utf-8
```

### Consultar en modo Verbose el Recurso/Servicio/API/etc
***Request***
```
curl -v http://35.202.138.44/wp-admin/install.php || curl --verbose http://35.202.138.44/wp-admin/install.php
```
***Output***
```
*   Trying 35.202.138.44:80...
* TCP_NODELAY set
* Connected to 35.202.138.44 (35.202.138.44) port 80 (#0)
> GET /wp-admin/install.php HTTP/1.1
> Host: 35.202.138.44
> User-Agent: curl/7.68.0
> Accept: */*
>
* Mark bundle as not supporting multiuse
< HTTP/1.1 200 OK
< Date: Wed, 22 Jun 2022 22:37:24 GMT
< Server: Apache/2.4.7 (Ubuntu)
< X-Powered-By: PHP/5.5.9-1ubuntu4.14
< Expires: Wed, 11 Jan 1984 05:00:00 GMT
< Cache-Control: no-cache, must-revalidate, max-age=0
< Pragma: no-cache
< Vary: Accept-Encoding
< Transfer-Encoding: chunked
< Content-Type: text/html; charset=utf-8
<
</>RESPONSE
```

### Descargar el recurso sin setear el nombre del recurso remoto
***Request***
```
curl -LO http://35.202.138.44/wp-admin/install.php
```
***Output***

![image](https://user-images.githubusercontent.com/27710797/175167319-bf90f639-c434-48c0-84ad-c47f88b80393.png)

### Descargar el recurso seteando el nombre del recurso remoto
***Request***
```
curl -L -o index_wordpress.html http://35.202.138.44/wp-admin/install.php
```
***Output***

![image](https://user-images.githubusercontent.com/27710797/175167944-2bf16e7b-0556-4b3f-a011-d427f7564ee9.png)



