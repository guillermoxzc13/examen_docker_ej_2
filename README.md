# examen_docker_ej_2



### Creación de Imágenes:

En primer lugar, creamos las imágenes necesarias para nuestros servicios utilizando los siguientes comandos de Docker:

1. **API REST:**
    ```bash
    docker build . -t restapi
    ```

2. **API SOAP:**
    ```bash
    docker build . -t soapapi
    ```

3. **Cliente:**
    ```bash
    docker build . -t client
    ```

4. **MySQL:**
    ```bash
    docker build . -t mysql
    ```

### Despliegue con Docker Swarm:

Luego, procedemos a desplegar nuestros servicios utilizando Docker Swarm:

1. **Inicialización de Swarm:**
    ```bash
    docker swarm init
    ```

2. **Despliegue con Docker Stack:**
    ```bash
    docker stack deploy -c docker-compose.yml mis-servicios
    ```

### Información Adicional:

- El servidor SOAP está configurado para escuchar en el puerto 4000.
- El servidor web está alojado en `localhost:8080`.

