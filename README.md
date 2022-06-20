# Laboratorio 3 Criptografia

##### Table of Contents  
[Codigo de Hash](##Codigo de Hash)  
[Driagrama de Flujo y Casos de Uso](##Driagrama de Flujo y Casos de Uso)  
[Comparativa de Rendimiento](##Comparativa de Rendimiento)  
 
<a name="Codigo de Hash"/>
<a name="Driagrama de Flujo y Casos de Uso"/>
<a name="Comparativa de Rendimiento"/>

##### Table of Contents  
[Headers](#headers)  
[Emphasis](#emphasis)  
...snip...    
<a name="headers"/>
## Headers

## Codigo de Hash
EL Codigo es Realizado se puede ver y probar a traves del siguiente Link (Se requiere mail UDP):
https://drive.google.com/file/d/15rQPPuo-1b89UGR_H1eM1hpMcBK7mVQP/view?usp=sharing 
O bien cargando el archivo Lab3Cripto.ipynb en Google Colab.

Para la realizacion de pruebas se pueden utilizar los archivos testHash.txt o rockyou_mini.txt los cuales se incluyen dentro de este repositorio.

## Driagrama de Flujo y Casos de Uso:

El sistema busca integrar un sistema de mensajería que permita a los usuarios enviar y recibir de forma segura sus mensajes y archivos, para ello el sistema utiliza un modelo de tokens, en el cual cuando se envía un archivo o texto este genere un token a partir de un Hash y este es enviado junto al mensaje, una vez un mensaje es recibido por otro usuario, se verifica la integridad del archivo volviendo a calcular el token de modo que si este no es igual al recibido por el mensaje, se alerta al usuario indicando que el mensaje ha sido intervenido.

El funcionamiento del Hash, a grandes rasgos consiste en la recepción del mensaje, el cual es evaluado para identificar si este consiste en un texto o un archivo, luego en caso de ser un archivo este es transportado a un buffer para su lectura, luego se crean y seleccionas variables necesarias para el proceso de cálculos matemáticos y lógicos, luego el resultado obtenido se transforma a su equivalente en ASCII.

![Lab3Cripto drawio](https://user-images.githubusercontent.com/70248621/174465600-89491278-c33c-4433-a7c0-f31737bc7946.png)


## Comparativa de Rendimiento

Las comparativas de rendimiento se pueden encontrar tanto en el archivo de TablasComparativas.xlsx o TablasComparativas.pdf, tambien se puede observar a continuacion: 

![image](https://user-images.githubusercontent.com/70248621/174529341-c62edd71-61a1-498f-9942-17a4e90e57f6.png)

![image](https://user-images.githubusercontent.com/70248621/174529286-87884284-5bf2-4564-8546-3a26ec60fc93.png)
