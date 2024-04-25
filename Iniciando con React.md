#Conociendo React

React es una librería de JavaScript que se encarga de la vista de una aplicación web o móvil. Modifica el DOM (Document Object Model) de forma dinámica, es decir, nos permite hacer cambios en tiempo real a la vista de un archivo HTML, ahorrándonos tiempo ya que solo se volverá a renderizar el objeto a modificar y no la página completa. React también puede hacer uso de una extensión de sintaxis de JavaScript llamada JSX, la cual nos permite definir elementos de React como variables. JSX transforma texto formateado como HTML en un archivo de JavaScript en objetos que serán analizados por el renderizador para desplegarlos como elementos HTML.

En una terminal, lanza el comando npx create-react-app y el nombre que le quieras poner a tu folder a usar, cuidado que no tenga mayúsculas. Esto creará una aplicación de react básica

image

Si no cuentas con los paquetes necesarios, obviamente tendrás que instalarlos, en cuyo caso tu consola te preguntará si los quieres instalar.

image

Una vez creado tu folder, debería crearse la carpeta, y dentro de ella, la carpeta de tus módulos, una carpeta “public”, tus fuentes y tu json con los paquetes de instalación. Si observas en este último, tenemos las dependencias de react.

image

Dirígete a el archivo App.js en tu carpeta “src”, debería aparecerte lo siguiente.

image

Si en este momento corres el comando npm start, la consola iniciará un servidor local de desarrollo, lo compilará, y a continuación abrirá una página en tu navegador que se verá de la siguiente manera, mostrándonos un logo rotatorio y un link a la documentación de React.

image

Sin embargo, el enfoque de este primer laboratorio es empezar a familiarizarnos con React, por lo que modificaremos el return de la función App para que solo nos regrese nuestro saludo favorito como programadores.

image

Ahora solo debes guardar el archivo y volver a cargar la página que se abrió anteriormente, y con esto ya sabes la forma más básica de mostrar texto con React.

image

Sigamos, en lugar de hacer el renderizado desde una sola función, vamos a sacar provecho de la modulación que podemos hacer con React, iniciemos con la creación de un componente al que llamaremos Greeting, usaremos esta función en un segundo.

image

Ahora solo hay que cambiar el contenido de la función App de tal forma que invocamos la función Greeting.

image

Si observas la página, ahora se muestra lo que pusimos en la función Greeting, esto se debe a que al renderizar los contenidos de la función App, se crea un fragmento que se identifica como Greeting y contiene todo lo que se haya definido en la función del mismo nombre. Vamos a crear un segundo elemento y lo llamaremos Response, el cual lo llenaremos así.

image

Ahora solo hay que meterlo en la función App y listo, ¿verdad? Intentémoslo

image

image

Como puedes ver, no es algo tan simple, solo tenemos que hacer un cambio rápido a la función App, si la observas de cerca, te darás cuenta de que el renderizado piensa que la primera función es la única a poner en el HTML, para ello, hay que dejar en claro que hay más cosas en la función, simplemente hay que anidar la función a un contenedor de la siguiente forma.

image

Normalmente usaríamos un

, pero React tiene lo que llamamos un fragmento, el cual podemos definir como <React.Fragment> o simplemente <>, usar el fragmento tiene sus ventajas, pero el mayor de todos es que reduce el consumo de recursos y el tamaño del DOM, haciendo que la página cargue más rápido y a comparación del
, permite que regresemos múltiples elementos de JSX. Regresemos a la página, como puedes ver, se han desplegado los dos elementos que definimos sin problema, y con esto puedes dar por terminado este primer laboratorio.
image
