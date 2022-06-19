# Laboratorio 3 Criptografia
EL Codigo es Realizado se puede ver a traves del siguiente Link (Se requiere mail UDP):
https://drive.google.com/file/d/15rQPPuo-1b89UGR_H1eM1hpMcBK7mVQP/view?usp=sharing, luego se puede realizar las prubas del codigo utilizando Google Colab

## Driagrama de Flujo y Casos de Uso:

El sistema busca integrar un sistema de mensajería que permita a los usuarios enviar y recibir de forma segura sus mensajes y archivos, para ello el sistema utiliza un modelo de tokens, en el cual cuando se envía un archivo o texto este genere un token a partir de un Hash y este es enviado junto al mensaje, una vez un mensaje es recibido por otro usuario, se verifica la integridad del archivo volviedo a calcular el token de modo que si este no es igual al recibido por el mensaje, se alerta al usuario indicando que el mensaje ha sido intervenido.

El funcionamiento del Hash, a grandes rasgos consiste en la recepción del mensaje, el cual es evaluado para identificar si este consiste en un texto o un archivo, luego en caso de ser un archivo este es transportado a un buffer para su lectura, luego se crean y seleccionas variables necesarias para el proceso de cálculos matemáticos y lógicos, luego el resultado obtenido se transforma a su equivalente en ASCII.

![Lab3Cripto drawio](https://user-images.githubusercontent.com/70248621/174465600-89491278-c33c-4433-a7c0-f31737bc7946.png)


