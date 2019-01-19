Hacer que gpg pida la clave por la tty
========================================

Para que **gpg** pida la clave en la tty y no por las X11, debemos instalar **pinentry-tty** y configurarla::

	# apt install pinentry-tty
	Leyendo lista de paquetes... Hecho
	Creando árbol de dependencias       
	Leyendo la información de estado... Hecho
	Paquetes sugeridos:
	  pinentry-doc
	Se instalarán los siguientes paquetes NUEVOS:
	  pinentry-tty
	0 actualizados, 1 nuevos se instalarán, 0 para eliminar y 142 no actualizados.
	Se necesita descargar 46,8 kB de archivos.
	Se utilizarán 94,2 kB de espacio de disco adicional después de esta operación.
	Des:1 http://deb.debian.org/debian stretch/main amd64 pinentry-tty amd64 1.0.0-2 [46,8 kB]
	Descargados 46,8 kB en 0s (67,3 kB/s)
	Seleccionando el paquete pinentry-tty previamente no seleccionado.
	(Leyendo la base de datos ... 205390 ficheros o directorios instalados actualmente.)
	Preparando para desempaquetar .../pinentry-tty_1.0.0-2_amd64.deb ...
	Desempaquetando pinentry-tty (1.0.0-2) ...
	Configurando pinentry-tty (1.0.0-2) ...
	Procesando disparadores para man-db (2.7.6.1-2) ...

Debemos ahora cambiar la configuracion de pinentry le debemos decir que sea **/usr/bin/pinentry-tty** ::

	# update-alternatives --config pinentry
	Existen 3 opciones para la alternativa pinentry (que provee /usr/bin/pinentry).

	  Selección   Ruta                      Prioridad  Estado
	------------------------------------------------------------
	* 0            /usr/bin/pinentry-gnome3   90        modo automático
	  1            /usr/bin/pinentry-curses   50        modo manual
	  2            /usr/bin/pinentry-gnome3   90        modo manual
	  3            /usr/bin/pinentry-tty      30        modo manual

	Pulse <Intro> para mantener el valor por omisión [*] o pulse un número de selección: 3

Ahora ya podemos ejecutar el **gpg** y que la clave la pida en la misma tty::

	# exit
	$ gpg -d miarchivo-txt.gpg 
	gpg: AES encrypted data
	Enter passphrase

	Passphrase: 
	gpg: encrypted with 1 passphrase

	Hola este es un archivo para verificar la Criptografia

