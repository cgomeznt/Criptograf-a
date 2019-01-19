Como encriptar Gpg4win y Kleopatra para Windows
=================================

Qué es Gpg4win?
Gpg4win es una suite de software libre para Windows que funciona con GnuPG, e incluye las siguientes herramientas de cifrado de archivos:

* GnuPG, la herramienta de encriptación principal
* Kleopatra, un gestor de certificados OpenPGP y X.509
* GPA, un gestor alternativo de certificados OpenPGP y X.509
* GpgOL, un plugin para Microsoft Outlook para cifrar emails
* GpgEX, un plugin para Microsoft Internet Explorer para cifrar archivos

Pongamos dos personas que desean intercambiar información: emisora y receptor.

.. figure:: ../images/01.png

Para el receptor crearemos una clave GPG para poder encriptar y desencriptar archivos.

El emisor subirá la clave a un servidor de claves PGP para compartirla con todo el mundo.

Luego, El emisor enviará al receptor un archivo cifrado con la clave pública del receptor, que solo él podrá desencriptar. Y finalmente, el emisor desencriptará el archivo con su clave privada.

En resumen serían estos pasos:
* receptor crea su par de claves PGP pública/privada
* receptor sube su clave PGP pública a un servidor de claves PGP
* receptor comparten su clave PGP pública con y el emisor 
* emisor encripta un archivo con la clave PGP pública de receptor
* emisor envía el archivo encriptado a receptor
* receptor descifra el archivo con su clave PGP privada

Crea su par de claves PGP pública/privada
+++++++++++++++++++++++++++++++++++++++++

Subir su clave PGP pública a un servidor de claves PGP
++++++++++++++++++++++++++++++++++++++++++++++++++++++

Compartir su clave PGP pública con y el emisor 
+++++++++++++++++++++++++++++++++++++++++++++++

Encriptar el archivo con la clave PGP pública de receptor
++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Enviar el archivo encriptado al receptor
++++++++++++++++++++++++++++++++++++++++

Descifra el archivo con su clave PGP privada
++++++++++++++++++++++++++++++++++++++++++++



