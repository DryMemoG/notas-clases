# **Introducción a Python**
Python es un lenguaje de programación interpretado, dinámico y de alto nivel, que fue creado en 1991 por Guido van Rossum. Es un lenguaje de programación multiparadigma, lo que significa que admite diferentes enfoques para la resolución de problemas, como programación orientada a objetos, programación funcional, programación procedural, entre otros.

Python se utiliza ampliamente en diferentes áreas, como desarrollo web, análisis de datos, inteligencia artificial, aprendizaje automático, ciencia de datos, entre otras. Además, cuenta con una amplia comunidad de usuarios y desarrolladores que contribuyen a la creación de bibliotecas y módulos para su uso en diferentes aplicaciones.

Una de las ventajas de Python es su sintaxis sencilla y legible, lo que lo hace ideal para principiantes en programación y para aquellos que buscan un lenguaje fácil de aprender. También es conocido por su portabilidad, ya que puede ejecutarse en diferentes sistemas operativos, como Windows, Linux, macOS, entre otros.

## **Inicio Rápido**
Podemos comprobar si tenemos Python instalado en nuestra computadora accediento a la terminal (CMD, Símbolo del Sistema) y ejecutando el siguiente comando

```console
python --version
```
Si el resultado son algunos números significa que tenemos Python instalado y los números indican la versión instalada. En algunos casos podemos tener Python instalado pero al ejecutar el comando en el CMD no nos aparece nada, eso significa que no ha sido agregado al [PATH](https://datatofish.com/add-python-to-windows-path/) por lo que puedes arreglarlo añadiendo Python a las variables de entorno, si sabes lo que haces, o bien, reinstalar Python. 

Al momento en el que redacto esto, la versión más reciente de Python es la 3.11.2 (Marzo, 2023), pero como regla no escrita del trabajo de desarrollador, trabajaremos con la versión de Python TODO: 3.10.9. 
___
## **Entorno de Trabajo con Python**
Podemos trabajar de muchas maneras con Python, a través de un IDE, o a través de un editor de código. En este curso trabajaremos con un **[Script](https://es.wikipedia.org/wiki/Script)** de Python y el editor de código Visual Studio Code *(No es Visual Studio Comunity).*

Para configurar nuestro primer Script de Python debemos crear una carpeta, en nuestra ubicación de preferencia, y la nombraremos *python-grado* posteriormente, entraremos a Visual Studio Code y abriremos una carpeta: Archivo -> Abrir Carpeta. 

### **Configurando Visual Studio Code**
En el menú de Extensiones en Visual Studio instalaremos las siguientes extensiones: 
* Python
* Pylance
* indent-rainbow
* Spanish Language Pack for Visual Studio Code

Estas serán extensiones que nos ayudarán en el proceso de creación de programas con Python. 

Posteriormente en el explorador daremos clic derecho y seleccionamos la opción de Nuevo Archivo, y lo llamaremos hola-mundo.py y escribiremos el siguiente código:
```python
print("Hola Mundo!")
```
Y listo habremos creado nuestro primer código en Python. 

## Anexos: 
Menú de VSCode

![Menu](/static/menuvscode.png)

Nuevo Archivo

![New](/static/nuevo-archivo.png)