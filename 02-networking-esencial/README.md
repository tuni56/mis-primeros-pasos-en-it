# Módulo 2: Networking Esencial (O cómo viajan los datos sin perderse en el camino) 🌐

> *Entender cómo se comunican las computadoras es el superpoder secreto de cualquier persona en IT. Dejemos de ver a la red como "magia negra" y empecemos a entender el mapa.*

---

## Paso 0: El cartero y la dirección (¿Qué es una IP?)

Imaginá que querés enviarle una carta a una amiga. Necesitás su dirección postal: calle, número, ciudad y código postal. En el mundo digital, pasa exactamente lo mismo.

* **Dirección IP (Internet Protocol):** Es el número único que identifica a un dispositivo (tu compu, un servidor, tu celu) conectado a una red. 
* **IP Pública vs. IP Privada:** 
  * La **privada** es la que te asigna el router de tu casa (por ejemplo, `192.168.1.5`) para que los dispositivos locales se reconozcan entre sí.
  * La **pública** es la que ve el resto del mundo cuando salís a internet (la que te asigna tu proveedor de internet).

Para ver cuál es tu IP local en tu terminal (Git Bash o la que uses), podés ejecutar:

bash
ipconfig (Si estás en Linux o Mac, el comando equivalente es ifconfig o ip a).

## Paso 1: La libreta de contactos (¿Qué es el DNS?)
A las personas nos cuesta recordar números largos. Si para entrar a Google tuvieramos que tipear algo como 142.250.190.46, navegar por internet sería un dolor de cabeza.

DNS (Domain Name System): Funciona como la agenda de contactos de tu teléfono. Traduce nombres fáciles de recordar (como google.com o github.com) a la dirección IP numérica que las máquinas entienden de verdad.

Cuando ponés una URL en el navegador, ocurre una consulta invisible a un servidor DNS que dice: "Che, ¿sabés a qué IP apunta esta página?". Te devuelve el número, y ahí recién arranca la conexión.

## Paso 2: Las puertas de entrada (¿Qué son los puertos?)
Si una computadora fuera un edificio de oficinas, la IP sería la dirección de la calle y los puertos serían las distintas puertas o ventanillas de atención al público.

Un puerto es un número lógico (del 0 al 65535) que le indica a la computadora a qué programa o servicio debe entregarle los datos que acaban de llegar.

Algunos puertos ya tienen nombres y servicios universales asignados por convención:

Puerto 80: Tráfico web común (HTTP).

Puerto 443: Tráfico web seguro (HTTPS).

Puerto 22: Conexiones seguras por terminal (SSH, el que usás para conectarte a GitHub o servidores en la nube).

## Paso 3: Probando la conexión (El comando ping)
Cuando una aplicación no conecta o querés saber si un servidor está "vivo" y accesible en la red, la herramienta más clásica y directa es el ping.

El ping envía pequeños paquetes de datos a un destino y mide cuánto tardan en ir y volver (la famosa latencia o ping).

Probá correr esto en tu terminal para ver si llegás a Google:

Bash
ping google.com
Para frenarlo (porque se queda enviando paquetes indefinidamente en Windows), apretá las teclas:

Bash
Ctrl + C
Paso 4: Descubriendo quién responde (El comando curl)
Si querés ver qué responde un servidor web directamente desde la terminal, sin abrir el navegador, podés usar curl. Es ideal para probar APIs o verificar si una página responde correctamente.

Ejecutá el siguiente comando para consultar una página de prueba:

Bash
curl [https://api.github.com](https://api.github.com)
Vas a ver cómo la terminal te escupe un montón de datos en formato JSON. Eso significa que la red respondió y pudimos dialogar con el servidor con éxito.
