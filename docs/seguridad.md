# Seguridad del gestor

| Comprobación | Antes | Después |
|---|---|---|
| Cabecera Server | `nginx/1.30.5` |Server: nginx |
| /xmlrpc.php | AHTTP/1.1 403 Forbidden Server: nginx |  <html>
403 Forbidden|
| API REST de usuarios (`/wp-json/wp/v2/users`) | [{"id":1,"name":"adabelrie","url":"http:\/\/localhost:8080","description":"","link":"http:\/\/localhost:8080\/author\/adabelrie\/","slug":"adabelrie","avatar_urls":{"24":"https:\/\/secure.gravatar.com\/avatar\/f2ec7c20356e3277090cf3f7317a10cf792d8532f9de6016ec7b8cfc8bd1ca48?s=24&d=mm&r=g","48":"https:\/\/secure.gravatar.com\/avatar\/f2ec7c20356e3277090cf3f7317a10cf792d8532f9de6016ec7b8cfc8bd1ca48?s=48&d=mm&r=g","96":"https:\/\/secure.gravatar.com\/avatar\/f2ec7c20356e3277090cf3f7317a10cf792d8532f9de6016ec7b8cfc8bd1ca48?s=96&d=mm&r=g"},"meta":[],"_links":{"self":[{"href":"http:\/\/localhost:8080\/wp-json\/wp\/v2\/users\/1","targetHints":{"allow":["GET"]}}],"collection":[{"href":"http:\/\/localhost:8080\/wp-json\/wp\/v2\/users"}]}}] | |

| /wp-config.php | nginx: the configuration file /etc/nginx/nginx.conf syntax is ok nginx: configuration file /etc/nginx/nginx.conf test is successful | 403 Forbidden  |
| PHP en uploads |2 | |
| Edición de ficheros desde el panel |Si se puede editar | No se puede editar los ficheros|
| Límite de intentos de login | Sin límite | Me tengo que esperar 20 minutos |

## Medidas aplicadas y por qué

¿aparece la versión de nginx? Si aparece la version 
 ¿responde xmlrpc.php? Si responde 
 HTTP/1.1 403 Forbidden
Server: nginx/1.30.5
Date: Sun, 25 Oct 2026 18:34:06 GMT
Content-Type: text/html
Content-Length: 146
Connection: keep-alive
X-Content-Type-Options: nosniff
X-Frame-Options: SAMEORIGIN
¿aparece el nombre de tu usuario en la lista de usuarios pública? Si aparece mi nombre 

