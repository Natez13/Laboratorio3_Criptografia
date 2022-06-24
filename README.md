
# Laboratorio 3 Criptografia

## Indice  
[Codigo de Hash](#CodigodeHash)  
[Driagrama de Flujo y Casos de Uso](#DriagramadeFlujoyCasosdeUso)  
[Comparativa de Rendimiento](#ComparativadeRendimiento)  
[Funcionamiento del Hash y Prgrama](#mfh)
 
<a name="CodigodeHash"/>



# Codigo de Hash
EL Codigo es Realizado se puede ver y probar a traves del siguiente Link (Se requiere mail UDP):
https://drive.google.com/file/d/15rQPPuo-1b89UGR_H1eM1hpMcBK7mVQP/view?usp=sharing 
O bien cargando el archivo Lab3Cripto.ipynb en Google Colab.

Para la realizacion de pruebas se pueden utilizar los archivos testHash.txt o rockyou_mini.txt los cuales se incluyen dentro de este repositorio.


## Driagrama de Flujo y Casos de Uso:
<a name="DriagramadeFlujoyCasosdeUso"/>
El sistema busca integrar un sistema de mensajería que permita a los usuarios enviar y recibir de forma segura sus mensajes y archivos, para ello el sistema utiliza un modelo de tokens, en el cual cuando se envía un archivo o texto este genere un token a partir de un Hash y este es enviado junto al mensaje, una vez un mensaje es recibido por otro usuario, se verifica la integridad del archivo volviendo a calcular el token de modo que si este no es igual al recibido por el mensaje, se alerta al usuario indicando que el mensaje ha sido intervenido.

El funcionamiento del Hash, a grandes rasgos consiste en la recepción del mensaje, el cual es evaluado para identificar si este consiste en un texto o un archivo, luego en caso de ser un archivo este es transportado a un buffer para su lectura, luego se crean y seleccionas variables necesarias para el proceso de cálculos matemáticos y lógicos, luego el resultado obtenido se transforma a su equivalente en ASCII.

![Lab3Cripto drawio](https://user-images.githubusercontent.com/70248621/174465600-89491278-c33c-4433-a7c0-f31737bc7946.png)


## Comparativa de Rendimiento
<a name="ComparativadeRendimiento"/>
Las comparativas de rendimiento se pueden encontrar tanto en el archivo de TablasComparativas.xlsx o TablasComparativas.pdf, tambien se puede observar a continuacion: 
<br />
<br />

![image](https://user-images.githubusercontent.com/70248621/174529341-c62edd71-61a1-498f-9942-17a4e90e57f6.png)

![image](https://user-images.githubusercontent.com/70248621/174529286-87884284-5bf2-4564-8546-3a26ec60fc93.png)


## Funcionamiento del Hash y Prgrama

### Funcionamiento del Hash
<a name="mfh"/>
A grandes rasgos el código Hash se compone de 4 funciones más la función principal de Hash. 
De las 4 funciones una corresponde a una función de Shift de un Texto, dado un valor y el texto al cual realizar el Shift, retornando el Texto Shifteado; una Función de Padding la cual agrega un pad predeterminado a un texto y retornara un string de largo 10 caracteres, una función Interprete, la cual traducirá un número a 55 caracteres ASCII y por último una función de Efecto Avalancha la cual recibirá el texto el cual debe ser Hasheado y calculara un número único, para ello realiza diversas acciones como un Shift y una Inversión al texto, seleccionar un valor de Shift y un número, los cual aplicara diversas funciones matemáticas hasta obtener un número único asociado al texto inicial.
Luego la función principal de Hash primero verifica si el largo del texto de entrada tiene como mínimo 10 caracteres, de no ser así llama a la función de Padding, caso contrario ejecuta el proceso de Hasheo el cual primero llama a la función de Efecto Avalancha (La cual hace uso de la función de Shift) y luego llama a la función Interprete.

### Funcionamiento del Programa

El programa consta de un menú el cual tiene 5 opciones: 

-   1.- Hash a un String: Esta opción recibe directamente un string dado por el usuario y realiza el Hash devolviendo el Hash del string y la entropía del Hash resultante.
-   2.- Hash a varios String en un archivo de texto: Esta opción recibe un archivo .txt y realiza un Hash a cada línea dentro de este, retornando el Hash de cada uno y la entropía del Hash resultante.
-   3.- Hash a un Archivo: Esta opción recibe un archivo y lo transforma a un buffer en formato ASCII, y luego realiza el Hash al buffer, retornando el Hash y la entropía de este.
-   4.1.- Entropía a un String: Calcula la entropía de un string dado.
-   4.2.- Entropía a varios String en un archivo de texto: Calcula la entropía de cada línea dentro del texto.
-   4.3.- Entropía a un Archivo: Esta opción recibe un archivo y lo transforma a un buffer y Calcula la entropía del buffer
-   5 .- Salir: Esta opción termina el programa

### Video

En el video a continuacion se puede observar un ejemplo de uso del Hash junto al calculo de rendimineto:

[![image](https://i9.ytimg.com/vi_webp/a8RTXGUqz0I/mqdefault.webp?v=62b63c2e&sqp=CPCD2ZUG&rs=AOn4CLC4VNJuqUh1WJu1wPF7o23vGxiSHw)](https://www.youtube.com/watch?v=a8RTXGUqz0I)

