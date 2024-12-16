# Proyecto de imagga

Aplicación web que analiza imágenes utilizando el servicio de inteligencia artificial de Imagga.

## Requisitos

Asegúrate de tener instalado:

- Python 3.7 o superior
- pip (gestor de paquetes de Python)
- Docker

### Configuración de variables de entorno

```
API_KEY=
API_SECRET=
API_ENDPOINT=

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
