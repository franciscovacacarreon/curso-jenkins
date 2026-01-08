# Jenkis
- Servidor de automatización
- Se encarga de gestionar 
    - Compilación del código fuente
    - Ejecución de pruebas automatizadas
    - Despliegue automáticos -> de pruebas

# Integración Continua (CI) y Entrega Continua (CD)

# Pipeline

# Jobs
- Tarea automatizada -> Servidor Jenkins
    - Podria compilar
    - Ejecutar pruebas
    - Despliegue
    - Cualquier otro proceso
- Existen varios tipos de Jobs
    - Freestyle Project -> El más básico de fácil de configrar
    - Pipeline -> Usado para los flujos de CI CD -> Más avanzados con script en groovy
    - Maven Project -> Para proyectos Maven

# Comandos:

# Crear contenedor de Jenkins
docker run -d --name jenkins -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts

# Solucionar error de instalación
docker run -d --name jenkins -p 9090:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts --argumentsRealm.passwd.admin=admin --argumentsRealm.roles.admin=admin --httpPort=8080

