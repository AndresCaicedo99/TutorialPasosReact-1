# Como crear React App con Vite


1.) Creamos una nueva carpeta que va a contener nuestro proyecto

2.) Para empezar a trabajar debemos seleccionar la carpeta utilizando la terminal PowerShell

En esta imagen veremos que inicialmente al abrir PowerShell vamos tener por defecto la siguiente ruta, que seria; "nombre de nuestro dispositivo"/"system32" que es la carpeta en la cual se encuentra, en este caso. 
![image](https://user-images.githubusercontent.com/124592267/225476796-89007bcb-dce9-4c75-bfab-a99fcf892b8f.png)

Para poder seleccionar la carpeta donde deseamos trabajar debemos:
  -Copiar la direccion url de la carpeta con la que deseamos trabajar de esta manera
  
  ![image](https://user-images.githubusercontent.com/124592267/225478447-372863dd-434b-49f8-b257-0eb4dd6f56a1.png)

  Ahora debemos escribir el comando "cd" junto con la url de la carpeta que copias anteriormente. El comando quedaria de la   siguiente manera.
  
```
cd C:\Users\andre\OneDrive\Escritorio\ReactPrueba
```
  Damos enter para ejecutar el comando y debe salirnos la siguiente informacion
  
  ![image](https://user-images.githubusercontent.com/124592267/225479281-f8aa41bd-e64a-4726-9170-7eb73cb89976.png)

 Como vemos nos ecnotramos dentro de la carpeta en la cual vamos a trabajar. 
  
3.) Ahora debemos ejecutar el siguiente comando para que se creen los archivos de nuestra App en la carpeta

```
npx create-react-app app-de-prueba
```
En la parte de "app-de-prueba" se puede colocar cualquier nombre, para identificar esa carpeta de archivos, al ejecutar el comando veremos como se empiezan a instalar los archivos de la libreria que seleccionamos, como podemos ver en la siguiente imagen.

![image](https://user-images.githubusercontent.com/124592267/225497914-52ead00d-812f-4167-98c5-9116da6851b4.png)


Una vez finalizado debe aparecer la siguiente informacion con los comandos que ya podemos ejecutar, asi:

![image](https://user-images.githubusercontent.com/124592267/225498889-f05601a7-20fe-4f52-bd73-fce74e5e9a8b.png)

Después de la creación, el proyecto debería tener este aspecto:

![image](https://user-images.githubusercontent.com/124592267/225500637-95a2ae16-87be-45d7-ab91-09cad05ffe5d.png)

Para que el proyecto se compile, estos archivos deben existir con nombres de archivo exactos:

public/index.html es la plantilla de página;
src/index.js es el punto de entrada de JavaScript.
Puede eliminar o cambiar el nombre de los demás archivos.

Puede crear subdirectorios dentro de . Para reconstrucciones más rápidas, solo los archivos dentro son procesados por webpack. Debe colocar cualquier archivo JS y CSS dentro de src, de lo contrario webpack no los verá.srcsrc

Sólo se pueden utilizar los archivos que hay dentro desde . Lea las instrucciones a continuación para usar activos de JavaScript y HTML.publicpublic/index.html

Sin embargo, puede crear más directorios de nivel superior. No se incluirán en la compilación de producción, por lo que puede usarlos para cosas como la documentación.

Si tiene Git instalado y su proyecto no forma parte de un repositorio más grande, se inicializará un nuevo repositorio que dará como resultado un directorio de nivel superior adicional..git

___________________________________________

**** SCRIPTS ****

Recordemos que en este punto debemos continuar dentro de la carpeta del proyecto y para ejecutar y ver la App debemos utilizar el siguiente comando, que ejecuta en modo desarrollo y lo apertura en la url no que da la terminal:

```
npm start
```
Si sale el siguiente error: 

![image](https://user-images.githubusercontent.com/124592267/225504709-8ac33742-6391-4c1c-85b1-879638f9bfb0.png)

El error se debe a que estamos dentro del directorio de la carpeta, pero no estamos dentro de la carpeta que creo el comando "npx create-react-app app-de-prueba". 

Debemos volver a posicionarnos el la carpeta del proyecto con el comando "cd" + "url de la carpeta del proyecto (incluyendo la nueva carpeta que se creo dentro de esta". Quedando asi:

![image](https://user-images.githubusercontent.com/124592267/225510308-865b43f5-4cd6-4133-9daf-03c749d74f39.png)

Ahora si debe ejecutarse correctamente mostrando la siguiente informacion, donde nos da una url que podremo abrir en el navegador y eso ya nos indicaria que tenemos todo ok

![image](https://user-images.githubusercontent.com/124592267/225513199-452e2928-2e59-492d-8159-464842452466.png)
















  ACA VOY!!!! MIN 10:20
  
  

¿Porque crear todo esto? React no permite hacer un Set up moderno para una web app, corriendo un solo comando. Es un concepto para crear el inicio de una aplicacion para poder centrarnos en el codigo y no en la configuracion de ciertas herramientas para construir el proyecto.

Template: son plantillas que traen la estructura de la aplicacion, Puede encontrar una lista de plantillas disponibles buscando "cra-template-*" en npm, segun la necesidad de desarrollo. La estructura de la App es la siguiente:

![image](https://user-images.githubusercontent.com/124592267/225467189-14daa70d-c99d-4463-8379-48a612deed43.png)

"Package"
"Package-lock"
Estos dos archivos estan relacionados al ecosistema de Node.js

".gitignore"
Es un arcgivo que sirve para git, ya que hay archivos como Package-lock y la carpeta de node_modules, que no se tienen que subir al repositorio.

"node_modules"
Esta carpeta contiene varios archivos, que son todos los archivos, que cuando se creo el template, se consideraron necesarios para la App. 

"src"
En la carpeta "src" se encuentra el contenido fuente de la App.

"public"
En la carpeta "public" se encuentran archivos que cualquier usario puede ver - por donde se va construir nuesta App. Aca montamos nuestra App - index.html

"Package.json": Es algo que se agrega para saber que dependencias se instalan
"Package.lock": Tambien conteine dependencias instaladas, junto a las url de donde las descarga

"index.js": Es el archivo que arranca la aplicacion

Todo esto es una forma sencilla de empeza una App con React sin configurar en demasia
