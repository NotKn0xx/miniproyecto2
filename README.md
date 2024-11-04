# miniproyecto2

actividad 2

toggle_led(): Esta función alterna entre encender y apagar un LED digital simulado. Cambia el texto del botón entre "ENCENDER LEDs" y "APAGAR LEDs" y muestra mensajes de estado en la consola. Funcionalidad relevante: Es una simulación de encendido y apagado, con un cambio de texto en el botón según el estado del LED.

change_brightness(value): Esta función ajusta la luminosidad del LED simulado según el valor del dial. Muestra en consola el nivel de brillo seleccionado. Funcionalidad relevante: Simula el ajuste de luminosidad del LED con el dial, y el valor se visualiza en un display LCD (QLCDNumber), haciendo que los usuarios vean los cambios en tiempo real.

toggle_timer(): Esta función activa o desactiva el temporizador que controla el cambio automático de las imágenes en pantalla. Funcionalidad relevante: Controla el temporizador (QTimer) que determina el cambio automático de imágenes cada 5 segundos (configurable). Al detener el temporizador, cambia el texto del botón a "INICIAR CAMBIO DE IMAGEN", y al activarlo, lo cambia a "DETENER CAMBIO DE IMAGEN".

change_image(): Esta función Cambia la imagen y el texto mostrados en la interfaz de usuario de manera aleatoria. Funcionalidad relevante: Selecciona al azar una imagen y un texto de una lista de diccionarios self.images, redimensiona la imagen y actualiza la visualización. Esto permite una presentación cíclica y dinámica de imágenes.


Actividad 1


Este es el readme de la actividad 1 del miniproyecto 2


En esta actividad tuvimos que programar un sistema de monitoreo en la red desde nuestro notebook a la raspberry pi y vice versa usando sensores de humedad, temperatura y distancia. Luego almacenando esos datos dentro de un log hecho mediante la biblioteca logging para luego con el uso del networking con la bilbioteca paramiko enviamos el archivo en tiempo real al notebook donde lo usamos para hacer un grafico y una tabla con los datos promediados

Luego la segunda parte de la actividad enviamos esos promedios mediante ssh a la raspberry que configurando unos umbrales para medir el nivel (Azul = bajo , Verde = medio y Rojo = alto) programamos en la raspberry pi que se encienda un led con el color estipulado según en que parte del umbral se encuentre el promedio sensado anteriormente


funciones y scrips principales tenemos 

el script descargarlog.py el cual nos permite descargar el log con todos los datos sensados anteriormente desde la raspberry pi hasta nuestro notebook

luego el script de graficos.py en donde no solo se hacen los gráficos y tablas para ver la variación y luego establecer los promedios sino que también se crea el log de los promedios en si para después enviarlo a la raspberry pi todo esto gracias a un menú hecho con anterioridad 

luego dentro de la raspberry tenemos el script de los sensores usado para recabar la información de los sensores previo a enviar al notebook


y luego tenemos el script de monitoreo usando el log con los promedios hechos en el notebook el cual activaran su led correspondiente según la variable sensada y el color correspondiente a en que parte del umbral se encuentra el promedio 

todo estos podemos usarlos a la vez en tiempo real para que funcione como sistema de monitoreo simple de temperatura humedad ambiental y distancia













