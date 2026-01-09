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

# Builds
- Es una ejecución de un job
- Cada vez que haga una ejecución se va a generar un build
    - Obtener el código fuente
    - Ejecuta los pasos que has definido
    - Registra la salida en el cosole 
    - Guardar los artefactos (Opcional)
    - Muestra el resultado del build en la interfaz

# Disparadores automáticos
- Polling SCM -> Revisar preiodicamente si hay cambios en el repo git
- Webhook -> Dispara el job cuando hay un cambio en el código
- Programación cron -> Se ejecuta en intervalos de tiempo
- Disparo por otro job -> un job podría ejecutar otro job cuando se termine
