# Documentación UD1 Lenguajes de Marcas

## Introducción a Lenguajes de Marcas

### Definición: 

Un lenguaje de marcas organiza información mediante una sintaxis basada en marcas o etiquetas.

### Clasificación de Lenguajes de marcas

|Tipo|Uso|Ejemplos|
|----|---|--------|
|Presentación|Dar formato a documentos de texto|HTML,CSS|
|Intercambio de información|Almacenar información de forma ordenada|XML, RSS|
|Documentación|Documentar proyectos|Markdown, Wikitext|

## Instalaciçon y configuración del entorno 

1. ### Instalción de VS Code 
   
    [VS code](https://code.visualstudio.com/)

    ![vs code](https://cdn-1.webcatalog.io/catalog/vs-code/vs-code-social-preview.png?v=1714776407457)
2. ### Instalción de plugins
    
    - La instalación hay que acceder a VS code -----> Apartado de plugins ------> Busca en los plugins el nombre y le damos a isntalr
    #### Enlaces
      - [LivePriview](https://marketplace.visualstudio.com/items?itemName=ms-vscode.live-server)
      - [HTML CSS Support](https://marketplace.visualstudio.com/items?itemName=ecmel.vscode-html-css)
      - [XML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-xml)
      - [Markdown all in one](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
  
    |Nombre|Def|foto|
    |------|---|----|
    |Live preview|Sirve para la previsualización del código en formato visual con el que tiene que salir.|![LivePreview](img/live.png)|
    |HTML CSS Support|Es un complemento que se instala en el editor para añadir funciones extra, mejorar la ayuda visual y agilizar la escritura de código web.|![HTML CSS Support](img/html.png)|
    |XML|Herramienta que añade soporte avanzado para leer, escribir, validar y dar formato a documentos en este lenguaje de marcado|![XML](img/xml.png)|
    |Markdown all in one|Es una extensión muy popular para editores de código como Visual Studio Code que reúne las herramientas esenciales para escribir y editar archivos en formato Markdown de forma rápida y cómoda|![MarkDown all in one](img/Markdown.png)|

3. ### Instalar Git
```bash
sudo apt install git
```
4. ### Configurar repositorio git.
   #### (en la carpeta principal del proyecto)
```bash
git init
git add .
git commit -m "Comentario discreptivo"
```
5. ### Conectar con GitHub
```bash
git remote add origin https://github.com/Dasdas08XD/LM-UD1.git
git branch -m main
git push -u origin main
```
6. ### Como usar solo un comando de guardado y subida.
   En este orden usar:
```bash
git config --global alias.acp '!git add . && git commit -m "$1" && git push -u origin main #'
```
- Así se guarda un comando con la ruta (acp) , se puede cambiar el nombre por otro. En este caso usé acp como sinónimo de: Add . - Commit - Push 
  
- El símbolo de "$1" indica que ese espacio de introucir el nombre de guardado, se reserva para introducir después.
  
- La '!....#' del comando es muy importante:
  - Este comando se tiene que ejecutar con comillas de solo una unidad ('). 
  - La exclamación es para indicarle a git "No trates esto como un solo comando de Git. Ejecuta todo lo que sigue directamente en la terminal del sistema operativo (Bash)."
  - Todo lo que escribas después de un # es ignorado por completo por la terminal. Sino push colocaría el mesnaje que pongamos en el comando y daría error.
```bash
git acp "Nombre que tu quieras"
```
7. ### Restaurar trabajo desde github

Git clone solo se hace una vez en un nuevo sitio de trabajo , luego solo tenemos que hacer un envio con (acp)
```bash
git clone (url del repositorio) 
```
Luego para las proximas veces solo hay que hacer el sigueinte comando para que se descarga, cuidado con modificar antes del pull peude haber contradicciones de los archivos.
```bash 
git pull
