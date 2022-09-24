Repositorio del proyecto FileMonitor.

El objetivo de este trabajo es la creación de un antivirus para detectar ransomware de cifrado utilizando archivos trampa en el sistema Android. 

Su funcionamiento se basa en un despliegue de archivos trampa (un fichero pdf) por todo el almacenamiento externo y moitorizar los eventos que suceden en los mismos. Cuándo un ransowmare ataque el almacenamiento externo del dispositivo, generará eventos en estos honeyfiles y la app FileMonitor (gracias a la implementación de patrones de detección ransomware) notificará al usuario pidiendo que pulse en ella para desinstalar la aplicación o aplicaciones que han sido calificadas como posibles autoras del ataque (para encontrar las aplicaciones sospechosas se hace uso de una whitelist en la que se meten todas las apps instaladas antes de monitorizar y una blacklist en la que se introduce toda aplicación instalada posteriormente a la monitorización).

Aquí encontrarás el proyecto de Android Studio, la apk y dos virus para probar.

Pasos para un uso correcto de la aplicación:

1. Instalar y ejecutar la apk de Filemonitor concediendo el permisos para gestionar el almacenamiento externo.

2. Darle al botón "Desplegar Trampa" para que cree los honeyfiles en el almacenamiento externo.

3. Darle al botón de "Play" para iniciar la monitorización.

En este momento, nuestro sistema de detección ransomware ya estará listo. Dejamos la apk corriendo en segundo plano y continuamos con el funcionamiento normal de nuestro teléfono sin problemas. Cuándo haya un posible ataque nos llegará una notificación que deberemos pulsar lo antes posible para desinstalar las apps pertinentes y estar a salvo.

Para probar los virus, una vez Filemonitor esté listo, ejecutamos las apk concediendo los permisos para que el virus pueda correr sin problemas. Así podrás comprobar como Filemonitor los detecta y te notifica en el menor tiempo posible. 

Cualquier persona con la intención de mejorar esta propuesta es bienvenida, aquí les dejo posibles mejoras que no han llegado a implementarse porque la tecnología del momento no lo permitía:

1. Desinstalar automáticamente las aplicaciones sospechosas en vez de tener que preguntar al usuario para dar su consentimiento. Esto permitiría que FileMonitor inhabilitase el ataque más rápido y así perder el menor número de archivos posible. Sin embargo, no se ha encontrado ningún permiso que el usuario pueda conceder a la app el cual permita que desisntale aplicaciones sin su consentimiento (desde Android lo ven como una conducta propia de aplicaciones maliciosas y no permiten dicha opción).

2. Cambiar los honeyfiles por archivos FIFO. Esto hará que cuando el ransomware lea cualquier archivo trampa (los cuales identifica como un archivo más) para poder cifrarlos, se quede bloqueado y no pueda progresar en el cifrado de archivos. Se aplicaría la misma contramedida de desisntalar la aplicación o aplicaciones sospechosas. Esto tendría una gran ventaja ya que si el archivo trampa es el primero o uno de los primeros que lee, coneseguiríamos detener el ataque con un número de archivos perdidos prácticamente inexistente. Sin embargo, no se ha podido implementar esta opción por el formato FAT32 de la memoria externa de los smartphones que impide la creación de archivos FIFO.

*** El material se ofrece con fines educativos y de investigación. No me responsabilizo de su uso indebido. ***
