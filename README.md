# Principales protocolos de internet
___
### FTP puerto 21
El protocolo de transferencia de archivos (FTP) es un protocolo de red estándar usado para transferir archivos entre un cliente y un servidor  en una red de computadoras.

La transferencia de archivos puede realizarse desde cualquiera de estos tres métodos
*Stream mode: Los datos son enviados como un flujo continuo, relevando al FTP de hacer cualquier proceso. Todo el procesamiento se le deja al TCP. No es necesario un indicador de fin de archivo, a menos que los datos se dividan en registros.
*Block mode: El FTP divide los datos en múltiples bloques(bloque de cabecera, recuento de bytes, y campo de datos) y luego lo pasa al TCP.
*Compresed mode: Los datos se comprimen usando un algoritmo simple.
![FTP alt](https://upload.wikimedia.org/wikipedia/commons/thumb/c/c5/Modelo_ftp.jpg/400px-Modelo_ftp.jpg)
 
##### Login
FTP usa un esquema de nombre de usuario y contraseña normal para conceder el acceso. El nombre de usuario se envía al servidor usando el comando USER, y la contraseña se envía usando el comando PASS. Si la información dada por el cliente es aceptada por el servidor, el servidor enviara un saludo al cliente y la sesión iniciará.
___


### SSH puerto 22
Secure Shell (SSH) es un protocolo de red criptograáfica para operar servicios de red de forma segura sobre una red insegura.
SSH proporciona un canal seguro sobre una red insegura en una arquitectura cliente-servidor conectando un cliente SSH con un servidor SSH. Las aplicaciones comunes incluyen inicio de sesión remoto por linea de comando y ejecución remota de comandos.
##### Usos
* Acceso a un shell por un host remoto
* Ejecución de lineas de comando simple en un host remoto
* Para crear inicios de sesión automatices a un servidor remoto
* Ralizar copias de seguridad, copias de manera efectiva y eficiente en conjunto con rsync
* Para navegar en la we a través de una conexión proxy encriptada con clientes SSH que soporten el protocolo SOCKS.
* Para montar de manera segura un directorio en un servidor remoto como un sistema de archivos en una computadora local usando SSHFS
* Para monitoreo remoto automatizado y mantenimiento de servidores.
* Para el desarrollo en dispositivos móviles que soportan SSH.
___


### Telnet puerto 23
Telnet es un protocolo de la capa de aplicación usado en internet o en redes de área local
para proveer una comunicación bidireccional interactiva orientada al texto usando una conexión de terminal virtual. Los datos de usuario son intercalados dentro de la banda con el control de información Telcon, una conexión de datos  byte oriented de 8-bit sobre el TCP.
___


### SMTP puerto 25
Protocolo de transferencia de correo simple (SMTP) es un estándar internacional para la transmisión de correo electrónico. 
SMTP usa el puerto TCP 25 por defecto. El protocolo para el envío de correo es el mismo, pero usa el puerto 587.

Una transacción SMTP consiste en una secuencia de 3 comandos/respuestas.
1. Comando MAIL, para establecer la dirección de retorno, también conocida como ruta de retorno.
2. Comando RCTP, para establecer un destinatario del mensaje, este comando puede ser usado múltiples veces, una por cada destinatario. La dirección también es parte del sobre.
3. DATA para señalar el comienzo del mensaje: el contenido del mensaje. Consiste en una cabecera de mensaje y una cuerpo de mensaje separado por una linea en blanco. DATA es en realidad un grupo de comandos, y el servidor responde doble, uno para el comando DATA, para hacer saber que esta listo para recibir el texto, y una segunda vez después de en fin de la secuencia de datos, para aceptar o rechazar el mensaje.
![SMTP alt](http://social.technet.microsoft.com/wiki/cfs-filesystemfile.ashx/__key/communityserver-wikis-components-files/00-00-00-00-05/5314.Smarthost.jpg)
___


### DNS puerto 53
El Sistema de Nombre de Dominio (DNS) es un sistema jerárquico de nomenclatura descentralizada para computadoras, servicios, o cualquier recurso conectado a internet o a una red privada.

El DNS tiene la responsabilidad de asignar los nombres de dominio y madera esos nombres a los recursos de internet designando nombres de servidores autoritarios para cada dominio. DNS puede ser actualizado rápidamente, permitiendo un a servicio de localización en la red cambiar sin afectar al usuario final.
DNS tiene un papel centran en los servicios de internet distribuidos tales como Cloud Services y redes de distribución de contenido.  Cuando un usuario entra a un servicio de internet distribuido usando una URL, el nombre de dominio de la URL es traducido a la dirección IP del servidor que esta cerca del usuario. La función principal del DNS es que  diferentes usuarios pueden recibir simultáneamente diferentes traducciones del mismo nombre de dominio. 
![DNS alt](http://queber.com/wp-content/uploads/blog_images/dns.png)
___



### HTTP puerto 80
El Protocolo de Transferencia de Hipertenso (HTTP) es un protocolo de aplicación para sistemas de información de hipermedios distribuidos, colaborativos. 
EL hipertenso es texto estructurado que usa enlaces lógicos (hyperlinks) entre nodos que contienen texto. HTTP es el protocolo para intercambiar o transferir Hipertexto.

HTTP funciona como un protocolo de solicitud-respuesta entre cliente-servidor, esta diseñado para permitir a los elementos de red intermedios mejorar o habilitar comunicaciones entre clientes y servidores.

##### Sesion HTTP
Una sesión HTTP es una secuencia de transacciones de solicitud-respuesta de red. Un cliente HTTP inicia una solicitud  estableciendo una conexión TCP a un puerto en particular (normalmente al puerto 80, en ocaciones al puerto 8080). Un servidor HTTP esta a la espera de mensajes de solicitud del cliente. Una vez recibida la solicitud, el servidor envía una respuesta, tal como "HTTP/1.1 200 OK", y un mensaje propio. El cuerpo del mensaje es normalmente el recurso solicitado, también puede regresar un mensaje de error o algún mensaje de información.
![http alt](https://docs.trafficserver.apache.org/en/latest/_images/httprvs.jpg)
 ___


### POP puerto 110
El Post Office Protocolo (POP) es un protocolo estándar de internet de nivel de aplicación usado por clientes locales de e-mail para recuperar e-mail de un servidor remoto mediante una conexión TCP/IP.

POP soporta los requerimientos de descarga y eliminación para acceder a buzones remotos.
Un servidor POP3 se encuentra en el puerto 110. La comunicación encintada para POP3 puede ser solicitada después de iniciar el protocolo, usando comandos STLS, si es que lo soporta, o por medio de POP3S, el cual se conecta con el servidor usando Transport Layer Security (TLS) o Secure Rockets Layer (SLS) en el puerto TCP 995.

Los mensajes disponibles para el cliente son arreglados cuando una sesión POO abre el buzón de correo, y son identificados por un numero de mensaje local para esa sesión o, de manera opcional, por un identificador único asignado al mensaje por el servidor POP. Este identificador único es permanente y único para permitir al buzón de correo acceder al mismo mensaje en diferentes sesiones POP. El correo es recibido y marcado par ser borrado por el numero de mensaje.
![POP alt](https://support.content.office.net/en-us/media/d82dd150-cbd4-4476-9955-4eb4618a1a60.gif)
___


### IMAP puerto 143
El Protocolo de Acceso de Mensajes de Internet es un protocolo de internet estándar usado por los clientes de internet para recuperar mensajes e-mail desde un servidor de correo sobre una conexión TCP/IP.
Virtualmente todos los clientes y servidores modernos de e-mail soportan IMAP. IMAP y POP3 son los dos protocolos estandar que mas han prevalecido para la recuperacion de emails, muchos proveedores de correo tales como Gmail, Outlook y Yahoo! Mail proveen soporte tanto para IMAP como POP3.
![IMAP alt](http://blog.dreamhosters.com/kbase/images/illustrations/email_illustration.gif)
___


### IRC puerto 194
Internet Relay Chat (IRC) es un protocolo de nivel de aplicacion que facilita la comunicacion en forma de texto. El proceso de chat trabaja sobre un modelo de red cliente-servidor. Los clientes IRC son programas que el usuario puede instalar en su sistema. Estos clientes se conectan al servidor de chat para transferir mensajes a otro cliente.

___


##### Fuentes:

https://en.wikipedia.org/wiki/File_Transfer_Protocol
https://en.wikipedia.org/wiki/Secure_Shell
https://en.wikipedia.org/wiki/Telnet
https://en.wikipedia.org/wiki/Simple_Mail_Transfer_Protocol
https://en.wikipedia.org/wiki/Domain_Name_System
https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol
https://en.wikipedia.org/wiki/Post_Office_Protocol
https://en.wikipedia.org/wiki/Internet_Message_Access_Protocol
https://en.wikipedia.org/wiki/Internet_Relay_Chat
