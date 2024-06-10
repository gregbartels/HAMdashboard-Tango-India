 ## Tango India Dashboard


EL primer dashboard gratuito  para todos los radioaficionados en zona TI lanzado por TI3GB

Este proyecto es una modificación del [HAMdashboard](https://github.com/VA3HDL/hamdashboard) original de VA3HDL, reutilizado con su aprobación.  Este proyecto se distribuye bajo la misma licencia.


![image](https://github.com/gregbartels/HAMdashboard-Tango-India/assets/78452640/60b7dc0c-89b4-4f51-8ae3-883bb6c6c0f6)



Presentacion del proyecto ( idioma ingles) 

[YouTube - Presentation video](https://www.youtube.com/watch?v=sIdqMQTGNSc)


### Instrucciones:
1. Simplemente descargue los archivos del repositorio de Github (hamdash.html, config.js y wheelzoom.js) y manténgalos juntos en la misma carpeta.
2.  Abra el archivo config.js con cualquier editor de texto (como el Bloc de notas)
3.  en la linea #1, modifique ###const topBarCenterText = `TI3GB - EJ89AU`;    por su callsing y Grilla ( Grid). Guarde los cambios.

5. Abre hamdash.html con cualquier navegador de tu preferencia y listo.
6. Con cualquier editor de texto (como el Bloc de notas) puede cambiar las imágenes de origen (pueden ser más de una por cuadro) o las opciones de menú del archivo config.js.


Video de configuracion ( EN INGLES) Proximamente en idioma español por  TI3GB
[YouTube - Configuration instructions contributed by Jason KM4ACK](https://youtu.be/9ZZXg60tN-o)

### Ayuda rápida:
* Haga doble clic en una imagen para expandirla a pantalla completa.
* Haga doble clic de nuevo para cerrar la vista de pantalla completa.
* Haga clic derecho en una imagen para mostrar la siguiente. (En la última versión es posible agregar varias imágenes por caja).
* El contenido se actualiza automáticamente cada 5 minutos.
* Sencillo y facil de utilizar

Agradecimientos especiales a Pablo, VA3HDL por su apoyo y dedicacion en este proyecto al compartirlo con otros radioaficionados.

Solución para problemas de incrustación de Pi-Star en iFrame:
Este error puede ocurrir si el servidor tiene ciertas medidas de seguridad, como la cabecera x-frame-options, que evita que su contenido se incruste en otros sitios web mediante iframes.

Inicia sesión en Pi-Star vía SSH y luego ejecuta este comando para cambiar al modo de lectura/escritura:

# rpi-rw
En el archivo /etc/nginx/default.d/security.conf comenta la línea a continuación con un "#" al frente, así:


 # add_header X-Frame-Options  "SAMEORIGIN";
 
Ejecuta este comando para volver al modo de solo lectura:

 # rpi-ro
Luego reinicia el Pi-Star.

Más sobre la incrustación en iFrame:
Hay muy poco que se puede hacer del lado del cliente si el sitio fuente no permite incrustar el sitio dentro de otra página (como el panel de control), especialmente si el usuario no puede cambiar la configuración del servidor (la mayoría de los casos).

Como solución para estos problemas, he probado ejecutar un proxy local en mi computadora para eliminar la cabecera x-frame-options que viene del servidor fuente y funcionó bien en algunos casos. Pero configurar un proxy añade otra capa de complejidad a la configuración.

## Actualizaciones

# Registro de cambios 2024.06.09:

Actualizacion del codigo para soportar videos  por VA3HDL



# Registro de cambios 2024.05.27:
Se movieron las partes de configuración del código JavaScript a su propio archivo "config.js" para que sea fácil de actualizar después de actualizaciones al código principal. Sugerido por Lou KI5FTY.
Mejora en la usabilidad del menú.

# Registro de cambios 2024.05.25:
Se eliminaron dependencias de fuentes instaladas localmente. Las fuentes ahora se cargan directamente desde Google Fonts para garantizar la consistencia.
Capacidad de añadir múltiples imágenes por posición. Las imágenes se rotan automáticamente cada 30 segundos.
La actualización automática ahora se pausa automáticamente al cambiar a un sitio web (desde el menú) o cuando una imagen se amplía a pantalla completa.
Se movieron las variables de configuración a la parte superior del script y se añadió un comentario adicional para facilitar la configuración inicial.
Se añadió un menú a la derecha de la página. Ahora el menú de la izquierda tiene enlaces de radioaficionados y el menú de la derecha tiene enlaces meteorológicos.
