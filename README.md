# frontend-devops
# Tienda Perritos - Frontend

Este repositorio contiene la interfaz de usuario para la plataforma de Tienda Perritos. La arquitectura de esta aplicación está diseñada para desplegarse mediante contenedores en Amazon EKS, consumiendo los servicios del backend a través de un LoadBalancer interno.

El catálogo interactivo de la tienda garantiza una navegación fluida y una correcta visualización de los productos para asegurar la mejor experiencia de usuario en la selección de artículos.

##  Tecnologías y Arquitectura
- **Servidor Web:** Nginx (configurado para proxy inverso)
- **Contenedores:** Docker (AWS ECR)
- **Orquestador:** Kubernetes (Deployment, Service tipo LoadBalancer, HPA)
- **CI/CD:** GitHub Actions

##  Estructura del Despliegue en EKS
El tráfico web es recibido por un balanceador de carga público aprovisionado por AWS, el cual redirige las peticiones a los pods del frontend gestionados por el HPA (Horizontal Pod Autoscaler) para soportar alta demanda concurrente.
