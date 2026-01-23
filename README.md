# Integración de FTP con servidor web

### Flujo de Publicación Web mediante FTP

**Objetivo:** Publicar contenido HTML accesible vía web utilizando FTP para la transferencia.

**Procedimiento realizado:**
![](https://raw.githubusercontent.com/JosecarlosGlr/Integraci-nDeFTPConServidorWeb/refs/heads/main/3.png)

1.  **Configuración del Entorno:** Se instaló el servidor web Apache2 y se configuró FileZilla Server para que el directorio raíz del usuario FTP apuntara al `DocumentRoot` del servidor web (`/var/www/html`). Se otorgaron permisos de escritura al directorio.

![](https://raw.githubusercontent.com/JosecarlosGlr/Integraci-nDeFTPConServidorWeb/refs/heads/main/1.png)
2.  **Transferencia (Upload):** Mediante FileZilla Client, se subió el archivo `prueba.html` a través del puerto 21. El servidor FTP escribió el archivo físicamente en el directorio `/var/www/html`.

![](https://raw.githubusercontent.com/JosecarlosGlr/Integraci-nDeFTPConServidorWeb/refs/heads/main/3.png)
3.  **Acceso (HTTP):** El servidor Apache detectó el nuevo archivo en su directorio público y lo sirvió al navegador al realizar la petición `GET /prueba.html` por el puerto 80 via HTTP.

**Conclusión:**
Este flujo demuestra la integración clásica entre servicios de transferencia (FTP) y servicios de publicación (HTTP), donde el FTP actúa como mecanismo de despliegue de contenido.
