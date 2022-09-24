Repositorio del proyecto FileMonitor.

El objetivo de este trabajo es la creación de un antivirus para la detección de ransomware de cifrado utilizando archivos trampa en el sistema Android. 

Su funcionamiento se basa en un despliegue de archivos trampa (un fichero pdf de ejemplo) por todo el almacenamiento externo y la monitorización de los mismos. Cuándo un ataque ransomware ataque el almacenamiento externo del dispositivo, la aplicación (gracias a la implementación de patrones de detección ransomware) notificará al usuario y le pedirá que desinstale con la mayor urgencia posible las aplicaciones 

Aquí encontrarás el proyecto de Android Studio, la apk y dos virus para probar.

Pasos para un uso correcto de la aplicación:

1. Instalar y ejecutar la apk de Filemonitor concediendo el permisos para gestionar el almacenamiento externo.

2. Darle al botón "Desplegar Trampa" para que cree los honeyfiles en el almacenamiento externo.

3. Darle al botón de play para iniciar la monitorización.

En este momento, nuestro sistema de detección ransomware ya estará listo. Dejamos la apk corriendo en segundo plano y continuamos con el funcionamiento normal de nuestro teléfono sin problemas. Cuándo haya un posible ataque nos llegará una notificación que deberemos pulsar lo antes posible para desinstalar las apps pertinentes y estar a salvo.

Para probar los virus, una vez Filemonitor esté listo, ejecutamos las apk concediendo los permisos para que el virus pueda correr sin problemas. Así podrás comprobar como Filemonitor los detecta y te notifica en poco tiempo. 

*** El material se ofrece con fines educativos y de investigación. No me responsabilizo de su uso indebido. ***
