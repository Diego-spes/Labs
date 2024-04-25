# Primeros pasos

React es una librería de JavaScript que se encarga de la vista de una aplicación web o móvil. Modifica el DOM (Document Object Model) de forma dinámica, es decir, nos permite hacer cambios en tiempo real a la vista de un archivo HTML, ahorrándonos tiempo ya que solo se volverá a renderizar el objeto a modificar y no la página completa.
React también puede hacer uso de una extensión de sintaxis de JavaScript llamada JSX, la cual nos permite definir elementos de React como variables. JSX transforma texto formateado como HTML en un archivo de JavaScript en objetos que serán analizados por el renderizador para desplegarlos como elementos HTML.

En una terminal, lanza el comando npx create-react-app  y el nombre que le quieras poner a tu folder a usar, cuidado que no tenga mayúsculas. Esto creará una aplicación de react básica

 ![image](https://github.com/Diego-spes/Labs/assets/74331292/81317c81-ec2b-4681-893e-0a7a5284970a)

Si no cuentas con los paquetes necesarios, obviamente tendrás que instalarlos, en cuyo caso tu consola te preguntará si los quieres instalar.

![image](https://github.com/Diego-spes/Labs/assets/74331292/0fb9d0ab-27b7-4cec-b78c-eb3f13d578bc)

 
Una vez creado tu folder, debería crearse la carpeta, y dentro de ella, la carpeta de tus módulos, una carpeta “public”, tus fuentes y tu json con los paquetes de instalación. Si observas en este último, tenemos las dependencias de react.

 ![image](https://github.com/Diego-spes/Labs/assets/74331292/651fc737-811c-4e1c-8019-af3acd3b06f9)

Dirígete a el archivo App.js en tu carpeta “src”, debería aparecerte lo siguiente.

![image](https://github.com/Diego-spes/Labs/assets/74331292/cf1b2ae5-d3d4-44d3-9d03-3065d31140f5)

 
Si en este momento corres el comando npm start, la consola iniciará un servidor local de desarrollo, lo compilará, y a continuación abrirá una página en tu navegador que se verá de la siguiente manera, mostrándonos un logo rotatorio y un link a la documentación de React.

![image](https://github.com/Diego-spes/Labs/assets/74331292/c5a3714e-cca0-43c0-9310-a0b205946771)

 
Sin embargo, el enfoque de este primer laboratorio es empezar a familiarizarnos con React, por lo que modificaremos el return de la función App para que solo nos regrese nuestro saludo favorito como programadores.

![image](https://github.com/Diego-spes/Labs/assets/74331292/48da387e-33d7-4682-9d5b-62c153511114)

 
Ahora solo debes guardar el archivo y volver a cargar la página que se abrió anteriormente, y con esto ya sabes la forma más básica de mostrar texto con React.

![image](https://github.com/Diego-spes/Labs/assets/74331292/4a55324b-a49c-4338-a8e1-f50faefa0098)

 
Sigamos, en lugar de hacer el renderizado desde una sola función, vamos a sacar provecho de la modulación que podemos hacer con React, iniciemos con la creación de un componente al que llamaremos Greeting, usaremos esta función en un segundo.

![image](https://github.com/Diego-spes/Labs/assets/74331292/cd568053-7c68-4de6-bd4a-80391cb288b4)

 
Ahora solo hay que cambiar el contenido de la función App de tal forma que invocamos la función Greeting.

![image](https://github.com/Diego-spes/Labs/assets/74331292/fe80d936-cd29-4742-a1d7-d23881f3290d)

 
Si observas la página, ahora se muestra lo que pusimos en la función Greeting, esto se debe a que al renderizar los contenidos de la función App, se crea un fragmento que se identifica como Greeting y contiene todo lo que se haya definido en la función del mismo nombre.
Vamos a crear un segundo elemento y lo llamaremos Response, el cual lo llenaremos así.

![image](https://github.com/Diego-spes/Labs/assets/74331292/0bb251d9-330a-4189-9e36-324180b817a4)

 
Ahora solo hay que meterlo en la función App y listo, ¿verdad? Intentémoslo

 ![image](https://github.com/Diego-spes/Labs/assets/74331292/085613d1-f58b-4c4e-98cc-2d7b386d888e)

 

 ![image](https://github.com/Diego-spes/Labs/assets/74331292/e62eb5bf-ee91-4622-962c-86678f48eab1)

 
Como puedes ver, no es algo tan simple, solo tenemos que hacer un cambio rápido a la función App, si la observas de cerca, te darás cuenta de que el renderizado piensa que la primera función es la única a poner en el HTML, para ello, hay que dejar en claro que hay más cosas en la función, simplemente hay que anidar la función a un contenedor de la siguiente forma.

![image](https://github.com/Diego-spes/Labs/assets/74331292/57f01ec3-3ede-4dc6-bddc-dcc36e2f1820)

 
Normalmente usaríamos un <div>, pero React tiene lo que llamamos un fragmento, el cual podemos definir como <React.Fragment> o simplemente <>, usar el fragmento tiene sus ventajas, pero el mayor de todos es que reduce el consumo de recursos y el tamaño del DOM, haciendo que la página cargue más rápido y a comparación del <div>, permite que regresemos múltiples elementos de JSX.
Regresemos a la página, como puedes ver, se han desplegado los dos elementos que definimos sin problema, y con esto puedes dar por terminado este primer laboratorio.

 ![image](https://github.com/Diego-spes/Labs/assets/74331292/5cd8cc08-27bf-474b-897b-16ca1cacf140)

