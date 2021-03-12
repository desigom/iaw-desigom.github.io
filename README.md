# iaw-desigom.github.io
 
 # Creación de un sitio web estático con MkDocs y GitHub Pages
 
 - MkDocs es un generador de sitios web estáticos que nos permite crear de forma sencilla un sitio web para documentar un proyecto. El contenido del sitio web está escrito en texto plano en formato Markdown y se configura con un único archivo de configuración en formato YAML.

- Pasos:

  - Creamos un proyecto nuevo:

    - En primer lugar vamos a situarnos en el directorio donde queremos crear nuestro proyecto.

    - Ejecutamos:

          docker run --rm -it -p 8000:8000 -v "$PWD":/docs squidfunk/mkdocs-material new .
      
  - Generamos la documentación:

        docker run --rm -it -v "$PWD":/docs squidfunk/mkdocs-material build

  - Publicamos la documentación en GitPages.

        docker run --rm -it -v ~/.ssh:/root/.ssh -v "$PWD":/docs squidfunk/mkdocs-material gh-deploy


