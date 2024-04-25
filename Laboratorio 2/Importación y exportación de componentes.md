Importación y Exportación de Componentes
Ya sabemos que React nos permite usar componentes, pero cuando desarrollamos una aplicación, haremos uso de una gran cantidad de funciones y lo último que queremos es trabajar en un archivo con miles de líneas, para ello, refactorizaremos un poco nuestro código de tal forma que las funciones las tomaremos de otros archivos.
Empecemos con la creación de un folder en la carpeta src al que llamaremos js, aquí guardaremos los archivos de JavaScript de laboratorios futuros, a continuación, crea otro folder, en este guardaras dos archivos JavaScript, los llamaremos greeting y response

![image](https://github.com/Diego-spes/Labs/assets/74331292/5ab38ae8-05ee-4783-b130-93f99e9c2cf0)


A continuación, corta y pega las funciones Greeting  y Response que tienes en tu archivo App.js en los archivos correspondientes

![image](https://github.com/Diego-spes/Labs/assets/74331292/a00043c5-c7f5-494e-aeb1-393e2bc2a325)


![image](https://github.com/Diego-spes/Labs/assets/74331292/761c2343-b6cd-48ff-8bd0-13f55fb6792c)

 
Recuerda que nuestra página está llamando al archivo App.js y no podrá compilar ya que ahora esta invocando funciones que no existen en el archivo, para arreglar eso, basta con ir a nuestros dos archivos y simplemente exporta sus componentes con las siguientes líneas de código al final de los archivos

 ![image](https://github.com/Diego-spes/Labs/assets/74331292/e2c5944b-6391-46a0-806c-00b10f13cb11)
 ![image](https://github.com/Diego-spes/Labs/assets/74331292/f37a8fb2-1211-4162-a861-e0489ed19124)


 
Ahora regresemos al archivo principal, importaremos ambas funciones, toma en cuenta que solo invocaras a la función exportada y hay que asignarle un nombre al importarla.

![image](https://github.com/Diego-spes/Labs/assets/74331292/8f3b0144-4140-4978-b091-28104a7816ed)

 
Y con esto, logramos que nuestros archivos sean más fáciles de leer, y si llegara a ocurrir un error, será más fácil encontrarlo.
