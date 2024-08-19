### README del Proyecto

---

#### Descripción del Proyecto

Este proyecto tiene como objetivo desplegar una API utilizando tecnologías clave de AWS como Lambda y DynamoDB, todo gestionado a través de Terraform, que es una herramienta de Infraestructura como Código (IaC). La API fue desarrollada en Node.js con TypeScript y está diseñada para manejar operaciones CRUD sobre una tabla en DynamoDB. La implementación se gestiona completamente en la nube de AWS, y para facilitar las pruebas, se puede consumir la API utilizando Postman.

El proyecto también incluye la configuración de pipelines CI/CD utilizando GitLab, lo que garantiza un flujo de despliegue automatizado y eficiente. Este es un ejemplo práctico que demuestra cómo utilizar herramientas modernas en un entorno DevOps para gestionar infraestructura y aplicaciones de manera escalable y repetible.

#### Documentación Técnica

---

##### 1. **Requisitos Previos**

- Tener instalados los siguientes programas:
  - Node.js y npm
  - Terraform CLI
  - Git
  - Postman (para pruebas)
  - Cuenta de AWS con permisos para crear y gestionar recursos.

##### 2. **Configuración del Entorno de Desarrollo**

1.  Clona el repositorio:

    ```bash
    git clone https://github.com/felifranco/aws_terraform_devops.git
    cd aws_terraform_devops
    ```

2.  Instala las dependencias necesarias para el proyecto Node.js:
    ```bash
    npm install
    ```

##### 3. **Despliegue de la Infraestructura**

1.  Configura tus credenciales de AWS:

    ```bash
    export AWS_ACCESS_KEY_ID=tu_access_key_id
    export AWS_SECRET_ACCESS_KEY=tu_secret_access_key
    ```

2.  Inicializa Terraform:

    ```bash
    terraform init
    ```

3.  Revisa el plan de despliegue para asegurarte de que los recursos que se van a crear son los correctos:

    ```bash
    terraform plan
    ```

4.  Despliega la infraestructura:
    ```bash
    terraform apply
    ```

##### 4. **Detalles Técnicos**

- **API en Node.js con TypeScript**: La API está construida en Node.js usando TypeScript. Los endpoints permiten realizar operaciones CRUD en una tabla DynamoDB.
- **AWS Lambda**: Se utiliza Lambda para ejecutar la lógica de la API sin necesidad de gestionar servidores.
- **DynamoDB**: Base de datos NoSQL de AWS utilizada para almacenar los datos de la API.
- **Terraform**: Herramienta utilizada para gestionar la infraestructura como código (IaC), permitiendo la creación de recursos en AWS de manera automática.
- **GitLab CI/CD**: Se configuró un pipeline para automatizar el proceso de testeo y despliegue.

##### 5. **Pruebas**

Para probar la API, puedes utilizar Postman con los siguientes endpoints (asegúrate de que la API está desplegada correctamente):

- **GET /items**: Recupera todos los ítems.
- **POST /items**: Crea un nuevo ítem.
- **PUT /items/{id}**: Actualiza un ítem existente.
- **DELETE /items/{id}**: Elimina un ítem.

Asegúrate de utilizar la URL del endpoint proporcionada por AWS API Gateway.

##### 6. **Limpieza de Recursos**

Una vez que hayas terminado, es recomendable limpiar los recursos creados para evitar costos innecesarios:

```bash
terraform destroy
```
