🏁 **Desafío de Investigación**
============================
--------------------------------

## **🔹 1. Diferencia entre HTTP y HTTPS**
![HTTP](images/http.png)

**HTTP** significa *HyperText Transfer Protocol*. Es el **protocolo** o *"lenguaje comun"* que permite la comunicación entre un navegador web y un servidor para cargar páginas en internet principalmente.
La desventaja de HTTP es que no cifra los datos transmitidos, entonces toda la información enviada como contraseñas o datos personales puede ser interceptada con facilidad.
Por otro lado, HTTPS significa *HyperText Transfer Protocol **Secure***. Es una version segura y mejorada de HTTP, usa los protocolos de **SSL/TLS**, sistema que protege la información que se envía entre un navegador y servidor haciendo que los datos viajen codificados y sean ilegibles para terceros. De esta manera, los datos que viajan entre el usuario y servidor se envían en forma cifrada, evitando que terceros puedan leer o modificar la comunicación.

### 🔐 Cifrado SSL/TLS en HTTPS
**TLS** es la *seguridad de la capa de transporte*, un protocolo criptográfico que asegura la conexión entre un servidor web y una aplicación por medio del cifrado de datos y se aplica a todos los datos. De esta forma los datos sensibles como credenciales de acceso, números de tarjeta, etc, quedan protegidos para que terceros no puedan interceptarlos.

La capa de *sockets seguros* (SSL) es una versión antigua de TLS. Ambos protocolos de seguridad funcionan practicamente de forma similar, sin embargo TLS tiene algoritmos de cifrado más robustos y suites más seguras, por lo que garantiza la privacidad de los datos y autenticación que SSL.

Ambos terminos suelen utilizarse indistintivamente ya que TLS se lanzó como una actualización a SSL 3.0.

Los certificados *SSL/TLS* protegen la transferencia de datos mediante tecnicas de cifrado simetrica y asimetrica. 

Un resumen del proceso:

1️⃣ El dueño de un sitio web compra un certificado SSL y lo instala en su servidor.

2️⃣ Cuando alguien visita el sitio, el navegador y el servidor hacen un “apretón de manos” SSL (SSL handshake) para ponerse de acuerdo en cómo comunicarse de forma segura.

3️⃣ Durante este proceso, el navegador pide el certificado y la clave pública del servidor para comprobar que es confiable.

4️⃣ Una vez verificado, el navegador y el servidor crean una clave de sesión secreta usando las claves pública y privada.

5️⃣ A partir de ese momento, toda la información que se envía se cifra con esa clave, y solo el navegador y el servidor pueden leerla. Esta clave solo sirve para esa sesión y se elimina cuando se cierra la conexión.

![Como funciona SSL](images/ssl.png)

### ✅ ¿Por qué HTTPS es más seguro?

HTTPS es más seguro porque garantiza confidencialidad, **autenticidad e integridad de la información.** Además, los navegadores muestran un candado en la barra de direcciones cuando un sitio usa HTTPS, indicando que la conexión es segura.
### 🔒 Ejemplo visual del candado en el navegador
Asi se ve un sitio seguro:

![ejemplo1](images/conexion-segura-1.png)
![ejemplo2](images/conexion-segura-2.png)

### ⚠️ ¿Qué sucede si un sitio no usa HTTPS?
Los sitios web sin certificado SSL/TLS funcionaran con HTTP transfiriendo datos en texto plano quedando vulnerables a que cualquiera en internet los pueda interceptar, existiendo un mayor riesgo de robo de datos y ataques como el pishing (fraude digital).

De todas formas, cuando un sitio no utiliza HTTPS, los navegadores suelen mostrar advertencias como “Sitio no seguro”, haciendo que la gente evite los sitios que no son seguros.

------------------------------------