🚀 Despliegue en AWS S3 y CloudFront con GitHub Actions

Este es un proyecto de prueba (no tiene contenido, el html es meramente de prueba). 
Repositorio usa GitHub Actions para desplegar automáticamente los archivos en un bucket S3 y actualizar la caché de CloudFront.

🛠️ Configuración del Pipeline
El archivo deploy.yml se encuentra en .github/workflows/. Este se ejecuta al hacer un push o pull request a la rama main.

🔹 Acciones del Pipeline
Configurar las credenciales de AWS:
Usa secretos almacenados en GitHub para autenticar AWS. (VER ***)

Sincronizar archivos con S3:
Copia los archivos al bucket desafio1aws, ignorando archivos sensibles.

Invalidar la caché de CloudFront:
Asegura que los últimos cambios se reflejen para los usuarios.

🔐 ***Configuración de Secretos en GitHub***

AWS_ACCESS_KEY_ID: Tu clave de acceso AWS.
AWS_SECRET_ACCESS_KEY: Tu clave secreta AWS.
CLOUDFRONT_DISTRIBUTION_ID: El ID de tu distribución CloudFront.

🚧 Flujo de Despliegue
Cambio en la rama main.
El pipeline se ejecuta automáticamente.
Se sincronizan los archivos en S3.
Se invalidan los cachés de CloudFront para los nuevos cambios.
