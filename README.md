# Word cloud de seguidores de Instagram
Hace poco empecé un proyecto personal con fines educativos en Instagram donde regularmente público tarjetas con tips de programacion en Python. Llegue a los 500 seguidores esta semana y me pareció digno de celebración. Me puse como objetivo hacer un word cloud con los nombres de mis seguidores, el problema era cómo obtener esa información.

¿Tendré que hacer web scrapping? ¿Podre descargar mi información de Instagram? Esas fueron algunas de las preguntas que me hice al momento de plantearme el problema y tras revisar un poco la aplicación y descubrí cómo descargar los datos fácilmente.

## Obteniendo los datos
Primero solicitamos la información de nuestra cuenta de instagram ingresando al siguiente enlace: siguientehttps://www.instagram.com/accounts/privacy_and_security/
Una vez que nos autenticamos veremos lo siguiente:

![alt text](https://miro.medium.com/max/700/1*KVeorxvitQWrFFMXeXM-hQ.png)

Vamos a la sección **Data Download** para solicitar una copia de nuestros datos y esto nos llevará a la siguiente página donde nos muestra la dirección de email a la que será enviada la copia.

![alt text](https://miro.medium.com/max/700/1*p1Pds3aDd4iU3yLuciZitw.png)

Una vez que verifiquemos nuestra identidad los datos tardaran alrededor de 48 horas en ser enviados a nuestro correo

![alt text](https://miro.medium.com/max/700/1*zigqkbPBF0wbZO_aHUZEaA.png)

Una vez pasado ese tiempo nos llegará un enlace para descargar la copia en un comprimido .zip que contendrá los siguientes archivos:

![alt text](https://miro.medium.com/max/550/1*MDFAAlA695oE9Tk0v3uO8A.png)

Para este ejercicio solo utilizaremos el archivo connections.json que contiene la información de nuestro seguidores en el siguiente formato:

![alt text](https://miro.medium.com/max/656/1*gP6zEOQvwisV_IGKUTb7RQ.png)

El contenido del JSON nos muestra dentro de **followers** los nombres de los usuarios como **key** y una fecha como **value**.
La fecha que vemos es la fecha en la que empezaron a seguir nuestra cuenta, para nuestra visualización esta fecha nos permitirá asignar el tamaño de cada nombre en la imagen.


