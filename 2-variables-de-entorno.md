# Variables de Entorno
### ¿Qué son las variables de entorno
# COMPLETAR
Es una variable dinámica que puede afectar al comportamiento de los procesos en ejecución en un ordenador. Son parte del entorno en el que se ejecuta un proceso.
### Para crear un contenedor con variables de entorno?

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

# COMPLETAR

# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR
![image](https://github.com/user-attachments/assets/43cbadd9-b272-4df0-a5ff-06c16a59ebc6)
![image](https://github.com/user-attachments/assets/8f8ad9bf-a88b-48f6-9143-4a6c408fa695)

### Crear un contenedor con mysql:8 , mapear todos los puertos
# COMPLETAR
![image](https://github.com/user-attachments/assets/f9cb4801-a541-48ba-a41d-0ad0bc36c84e)

### ¿El contenedor se está ejecutando?
# COMPLETAR
No, al ejecutar ´´´ docker ps -a ´´´ En el contenedor sql muestra Exited (1) 4 minutes ago
### Identificar el problema
# COMPLETAR
´´´´ docker logs sql8

2024-06-07 13:45:02+00:00 [Note] [Entrypoint]: Entrypoint script for MySQL Server 8.4.0-1.el9 started. 2024-06-07 13:45:04+00:00 [Note] [Entrypoint]: Switching to dedicated user 'mysql' 2024-06-07 13:45:04+00:00 [Note] [Entrypoint]: Entrypoint script for MySQL Server 8.4.0-1.el9 started. 2024-06-07 13:45:05+00:00 [ERROR] [Entrypoint]: Database is uninitialized and password option is not specified You need to specify one of the following as an environment variable: - MYSQL_ROOT_PASSWORD - MYSQL_ALLOW_EMPTY_PASSWORD - MYSQL_RANDOM_ROOT_PASSWORD

no tiene las suficientes variables de entorno. ´´´´
### Eliminar el contenedor creado con mysql:8 
# COMPLETAR
´´´´ C:\Users\LabP3E010\containers>docker rm sql8

sql8 ´´´´
### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

Previo a esto es necesario crear el archivo y colocar las variables en un archivo, **.env** se ha convertido en una convención estándar, pero también es posible usar cualquier extensión como **.txt**.
```
docker run -d --name <nombre contenedor> --env-file=<nombreArchivo>.<extensión> <nombre imagen>
```
**Considerar**
Es necesario especificar la ruta absoluta del archivo si este se encuentra en una ubicación diferente a la que estás ejecutando el comando docker run.

### Crear un contenedor con mysql:8 , mapear todos los puertos y configurar las variables de entorno mediante un archivo
# COMPLETAR
![image](https://github.com/user-attachments/assets/6ea3cb37-1e16-4612-9699-62a03ce5be33)
![image](https://github.com/user-attachments/assets/9c7ffa8b-6cbc-4816-886f-768ab248ac42)

# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR 
![image](https://github.com/user-attachments/assets/477cc617-e9e8-4555-b24a-62beaba796cd)

### ¿Qué bases de datos existen en el contenedor creado?
# COMPLETAR
![image](https://github.com/user-attachments/assets/c6226459-7a19-4b29-85b2-2375bd417055)
