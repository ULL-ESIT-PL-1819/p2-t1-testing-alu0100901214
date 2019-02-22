## p2-t1-testing-alu0100901214
### Sergio González Guerra   alu0100910214

[![Build Status](https://travis-ci.org/ULL-ESIT-PL-1819/p2-t1-testing-alu0100836400.svg?branch=master)](https://travis-ci.org/ULL-ESIT-PL-1819/p2-t1-testing-alu0100836400)

# Tutorial practica 2

## Introducción.
La práctica consiste en usar Node.js para convertir datos XML en formato JSON, haciendo uso de la metodología de desarrollo dirigida por pruebas (TDD). Para ello debemos instalar las dependencias necesarias.

## Creando nuestra carpeta de trabajo y cargando los archivos rdf.
- Primero debemos crearnos la carpeta '/database', donde guardaremos todo el código fuente:

  #mkdir databases
  
- También crearemos la carpeta '/data' dentro de '/database', donde guardaremos una serie de datos sobre libros en formato rdf:

  #mkdir data
  
- Descargaremos los archivos rdf de los libros dentro de la carpeta '/data':

  #curl -O http://www.gutenberg.org/cache/epub/feeds/rdf-files.tar.bz2
  
- Descomprimimos el contenido:

  #tar -xvjf rdf-files.tar.bz2
Esto nos creara una carpeta cache con todos los archivos rdf.

## Inicializar package.json .

- Uno de los primeros ficheros fuente que necesitaremos sera el package.json, lo inicializaremos con el siguiente código: 

![ini](./img2/packageJsonInicial.PNG)

- Instalamos chai para realizar los expect y mocha para los test y seguir la metodología TDD dentro de '/database':

  #npm init -y
  #npm install --save-dev --save-exact mocha@2.4.5 chai@3.5.0
  
- En la sección 'scripts' del package.json añadimos lo siguiente:

![scriptMocha](./img2/scriptMocha.PNG)

- Ahora la entrada de los test invocaran a mocha.

