Hasta ahora hemos visto como crear componentes que, en su mayoría, han sido estáticos, es decir, no cambian cuando lanzamos el sitio web. Para hacer que nuestro sitio tenga una forma de interactividad, iniciaremos con lo más simple, un botón que aumente un número.
Iniciaremos con la declaración del botón y un label al que se le modificará su contenido al presionarlo, recuerda crear un nuevo archivo y el folder que le corresponderá.

![image](https://github.com/Diego-spes/Labs/assets/74331292/330a8563-271e-45dd-97f0-18f7a2865c3d)

![image](https://github.com/Diego-spes/Labs/assets/74331292/24034f4c-7986-4c93-a32b-c886462180ec)

Para facilitarnos la vida los vamos a definir en la misma función, en un segundo verás por qué.
React cuenta con un hook llamado useState, el cual nos permite definir una variable de estado, la definimos dentro de la función Button de la siguiente forma.

![image](https://github.com/Diego-spes/Labs/assets/74331292/30ac3775-ffc4-4a4d-bee4-d2664cb1eb1a)

Con esto solo hemos definido la variable de estado y le hemos indicado que se inicie en 0, también definimos una función que nos servirá para alterar el estado. Si queremos que nuestro botón haga algo, debemos definirlo en una función, para ello invocaremos la función setJump dentro de una función distinta, la cual será llamada por el botón.

![image](https://github.com/Diego-spes/Labs/assets/74331292/fe09a76f-dd0a-4372-8058-11846ede766b)

Es un buen momento para explicar los corchetes; al trabajar con la sintaxis de JSX, podemos insertar código de JavaScript a ciertos segmentos de la vista que serán procesados por el renderizado, similar a lo que hacíamos con los archivos ejs. Si observas, definimos que al activar el onClick del botón, se invoca handleJump, lo cual modificará el valor de jumps ya que en la función se invoca al cambio de estado, mientras que en nuestro label invocamos al estado como tal para desplegarlo.
Vamos a poner nuestro botón 2 veces en una función Result y exportaremos la misma a nuestro archivo App.js para que puedas observarlo en acción.

![image](https://github.com/Diego-spes/Labs/assets/74331292/82c65f50-bfde-4443-8d2e-d4689cf9a865)


![image](https://github.com/Diego-spes/Labs/assets/74331292/9e7749b2-de85-4842-a448-75f268a7f55f)


Si haces click a cualquiera de los dos botónes, verás que incrementan de manera independiente a pesar de ser el mismo componente, recuerda que al trabajar con módulos pueden existir múltiples copias de uno mismo.

![image](https://github.com/Diego-spes/Labs/assets/74331292/fc7c5c0f-857e-40fa-839c-af14c72fea7f)

¿Pero que pasa si queremos que nuestros componentes hagan referencia al mismo valor? Imagina que quieres comprar un artículo en una tienda online, pero alguien más lo compra antes que tú justo cuando lo viste y no tienes forma de saberlo, seguramente querrás saber si queda algo en el inventario antes de darte una ilusión.
Vamos a duplicar nuestra función Button y la vamos a alterar un poco, de tal forma que solo quede el return.

![image](https://github.com/Diego-spes/Labs/assets/74331292/4a609548-7ebb-4e69-b365-d75996ec3787)

Ahora agregaremos otro hook de useState, pero este irá en nuestra función Result, el código es exactamente el mismo que antes solo que sus partes están en lugares distintos.


![image](https://github.com/Diego-spes/Labs/assets/74331292/16fcff06-5dc9-4aaa-b364-fac24d760f0f)


Sin embargo, nuestros botones compartidos aún no hacen nada, después de todo le quitamos su código y lo dejamos con el puro fragmento a renderizar, vamos a cambiar eso. En las entradas de tu función, define dos atributos que recibirán tanto el contador como la función que usarás.


![image](https://github.com/Diego-spes/Labs/assets/74331292/d130a83b-dcc9-4bb3-a445-445bd5db725c)


Ahora solo debes pasarle los atributos a la función desde su invocación, es muy importante que al pasar los atributos utilices el mismo nombre que definiste como tu entrada.

![image](https://github.com/Diego-spes/Labs/assets/74331292/9ea3c25e-a44c-4842-84fa-3c99b6a5f76c)


Y ahora, si presionas cualquiera de los dos botones, observarás que el valor de ambos se actualiza al mismo tiempo.

![image](https://github.com/Diego-spes/Labs/assets/74331292/42ff0bdd-1d80-420b-abfb-e16ee033d6d6)

Con esto puedes dar por terminado el laboratorio de botones, y como manejar los atributos de estado.
