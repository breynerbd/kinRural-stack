# Levantar el proyecto

Antes de iniciar el proyecto, verifica que se hayan completado los valores de configuración en los siguientes archivos:

- `kinRural-auth-service/src/AuthService.Api/appsettings.Development.json`
- `kinRural-auth-service/src/AuthService.Api/appsettings.json`
- `kinRural-client-user/.env`
- `kinRural-server-admin/.env`
- `kinRural-server-user/.env`

Una vez configurados los archivos, abre Docker y verifica que no existan contenedores utilizando los puertos **5070**, **3005**, **3006**, **5173** y **8081**.

Si deseas limpiar completamente el entorno de Docker, puedes ejecutar el siguiente comando:

```bash
docker stop $(docker ps -aq); docker rm $(docker ps -aq); docker rmi $(docker images -aq) -f; docker volume rm $(docker volume ls -q); docker network prune -f; docker system prune -a --volumes -f
```

Finalmente, dirígete a la carpeta:

```text
kinRural-stack
```

y ejecuta:

```bash
docker compose up --build
```
