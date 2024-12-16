# FINAL PROJECT

Aplicación web que analiza imágenes utilizando el servicio de inteligencia artificial de Imagga.

## Requisitos

Asegúrate de tener instalado:

- Python 3.7 o superior
- pip (gestor de paquetes de Python)
- Docker

### Configuración de variables de entorno

```
# MYSQL
AWS_MYSQL_URL=
AWS_MYSQL_PORT=
AWS_MYSQL_USER=
AWS_MYSQL_PASSWORD=
AWS_MYSQL_DB_NAME=

# S3
AWS_S3_REGION=
AWS_S3_BUCKET_NAME=
AWS_S3_ACCESS_KEY=
AWS_S3_SECRET_ACCESS_KEY=

# IMAGGA
IMAGGA_API_KEY=
IMAGGA_API_SECRET=
IMAGGA_ENDPOINT=

```

## Levantamiento del servidor

**Ejecutar la aplicación**: ejecutar el archivo principal `run.py`

   ```bash
      pip index.py
   ```

## Configuración del entorno con Docker

1. **Generar instancia de Docker**:

   ```bash
   docker build -t flask_meme_app .
   ```
2. **Ejecutar la Instancia**:

   ```bash
   docker run -it -p 5000:5000 flask_meme_app
   ```
3. **Ejecutar la instancia y almacenarla**:

   Este comando correra la instancia de Docker y la almacenara dentro del contexto de Docker.
   ```bash
   docker run -p 5000:5000 image-analyzer
   ```
### Enlace de la aplicacion

    http://localhost:5000


### Pasos para la verificación

Abra http://localhost:5000 en su navegador:
* Vera tres imágenes mostradas
* Haga clic en el botón "Analizar"
* Cada imagen mostrará sus dos etiquetas más relevantes con porcentajes de confianza.

imagen de resultado:
![Captura de la imagen levantada en local](/docs/result.png)
