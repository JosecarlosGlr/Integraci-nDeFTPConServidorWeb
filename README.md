# Integración de FTP con servidor web

### Flujo de Publicación Web mediante FTP

**Objetivo:** Publicar contenido HTML accesible vía web utilizando FTP como mecanismo principal para la transferencia y despliegue de archivos.

**Procedimiento realizado:**

![](https://raw.githubusercontent.com/JosecarlosGlr/Integraci-nDeFTPConServidorWeb/refs/heads/main/3.png)

1. **Configuración del Entorno:** He instalado y verificado el servidor web **Apache2** en Ubuntu mediante el comando `systemctl status apache2`. Se ha configurado FileZilla Server para que el directorio del usuario FTP coincida con el **DocumentRoot** de Apache (`/var/www/html`), asegurando que el servidor FTP tenga permisos de escritura sobre dicha ruta.

![](https://raw.githubusercontent.com/JosecarlosGlr/Integraci-nDeFTPConServidorWeb/refs/heads/main/1.png)

2. **Transferencia (Upload):** Utilizando **FileZilla Client**, me he conectado al sitio "Prueba Local" con el usuario `tester`. He procedido a subir el archivo `prueba.html` desde mi escritorio local hacia el directorio remoto. El log confirma que la transferencia finalizó correctamente y el archivo ya es visible en la estructura del servidor.

![](https://raw.githubusercontent.com/JosecarlosGlr/Integraci-nDeFTPConServidorWeb/refs/heads/main/2.png)

3. **Acceso y Verificación (HTTP):** Para comprobar el flujo, he accedido desde el navegador Firefox a la dirección `http://localhost/prueba.html`. El servidor Apache ha servido el archivo correctamente, mostrando el mensaje **"Hola Mundo - Esta web esta subida por FTP"**, lo que confirma que el contenido subido por FTP es procesado y publicado instantáneamente por el servidor web.

---

### Conclusión del Flujo de Publicación
Este ejercicio demuestra la integración clásica entre servicios de red: **FTP** actúa como el canal de gestión (puerto 21) para el despliegue de contenidos, mientras que **HTTP** (puerto 80) se encarga de la entrega final del contenido al usuario. Es un método eficiente para gestionar sitios web de forma remota sin necesidad de acceso directo por consola al servidor.
