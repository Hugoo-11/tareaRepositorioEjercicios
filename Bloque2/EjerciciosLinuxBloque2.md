# Ejercicios Linux

### Ejercicio 1

Muestra todas las interfaces de red activas y sus direcciones IP en el sistema.

**Comando:** `ip a`

![image.png](image.png)

---

### Ejercicio 2

¿Cómo mostrarías solo la información de la interfaz de red eth0 usando ip?

**Comando:** `ip a show enp0s3`

![image.png](image%201.png)

---

### Ejercicio 3

Configura manualmente la dirección IP 192.168.1.100/24 en la interfaz eth0 con ifconfig.

**Comando:** `sudo ifconfig eth0 192.168.1.100/24`

---

### Ejercicio 4

Envía 10 paquetes ICMP a la dirección IP 8.8.8.8 usando ping.

**Comando:** `ping -c 10 8.8.8.8`

![image.png](image%202.png)

---

### Ejercicio 5

Consulta la dirección IP de [www.example.com](http://www.example.com/) usando nslookup.

**Comando:** `nslookup www.example.com`

![image.png](image%203.png)

---

### Ejercicio 6

Muestra las conexiones TCP activas en el sistema usando netstat.

**Comando:** `netstat -t`

![image.png](image%204.png)

---

### Ejercicio 7

Descarga el contenido de la página principal de [www.example.com](http://www.example.com/) usando curl y guárdalo en un archivo llamado example.html.

**Comando:** `curl www.example.com -o example.html`

---

### Ejercicio 8

Muestra el nombre del host actual del sistema.

**Comando:** `hostname`

![image.png](image%205.png)

---

### Ejercicio 9

Obtén la información del registro del dominio example.com usando whois.

**Comando:** `whois example.com`

![image.png](image%206.png)

---

### Ejercicio 10

Cambia temporalmente el nombre del host a servidor01 usando hostname.

**Comando:** `sudo hostname servidor0`

---

### Ejercicio 11

Envía un ping a la dirección 192.168.1.1 y muéstralo en modo detallado (verbose).

**Comando:** `ping -v 192.168.1.1`

![image.png](image%207.png)

---

### Ejercicio 12

Muestra las estadísticas de la red, como la cantidad de paquetes transmitidos, usando netstat.

**Comando:** `netstat -s`

![image.png](image%208.png)

---

### Ejercicio 13

Realiza una consulta inversa para obtener el nombre de dominio asociado a la IP 8.8.8.8 usando nslookup.

**Comando:** `nslookup 8.8.8.8`

![image.png](image%209.png)

---

### Ejercicio 14

Configura temporalmente la máscara de subred 255.255.255.128 en la interfaz eth1 usando ifconfig.

**Comando:** `sudo ifconfig eth1 netmask 255.255.255.128`

---

### Ejercicio 15

Muestra las rutas de enrutamiento actuales del sistema usando netstat.

**Comando:** `netstat -r`

![image.png](image%2010.png)

---

### Ejercicio 16

Realiza una solicitud HTTP GET a la API de GitHub para obtener los repositorios de usuario123 usando curl.

**Comando:** `curl https://api.github.com/users/usuario123/repos`

---

### Ejercicio 17

Envía un ping a la dirección 2001:4860:4860::8888 (IPv6 de Google) con ping6 y limita los paquetes a 4.

**Comando:** `ping6 -c 4 2001:4860:4860::8888`

---

### Ejercicio 18

Obtén las estadísticas de los sockets activos en el sistema con netstat.

**Comando:** `netstat -an`

![image.png](image%2011.png)

---

### Ejercicio 19

Cambia temporalmente la dirección MAC de la interfaz eth0 a 00:11:22:33:44:55 usando ifconfig.

**Comando:** `sudo ifconfig eth0 hw ether 00:11:22:33:44:55`

---

### Ejercicio 20

Realiza una solicitud HTTP POST a https://httpbin.org/post enviando el usuario admin y la contraseña 12345 usando curl.

**Comando:** `curl -X POST -d "user=admin&password=12345" https://httpbin.org/post`

---

### Ejercicio 21

Consulta el nombre de dominio completo (FQDN) de tu sistema usando hostname.

**Comando:** `hostname -f`

![image.png](image%2012.png)

---

### Ejercicio 22

Muestra solo las conexiones activas en la interfaz eth0 usando netstat.

**Comando:** `netstat -i eth0`

![image.png](image%2013.png)

---

### Ejercicio 23

Muestra las conexiones activas con nombres de dominio en lugar de direcciones IP usando netstat.

**Comando:** `netstat -n`

![image.png](image%2014.png)

---

### Ejercicio 24

Configura una nueva puerta de enlace predeterminada con la dirección 192.168.1.1 usando ip route.

**Comando:** `sudo ip route add default via 192.168.1.1`

---

### Ejercicio 25

¿Qué comando usarías para ver todas las rutas configuradas en tu sistema?

**Comando:** `ip route`

![image.png](image%2015.png)

---

### Ejercicio 26

Configura una nueva ruta de enrutamiento estática a la red 10.10.10.0/24 pase por el gateway 192.168.1.1 en la interfaz eth0.

**Comando:** `sudo ip route add 10.10.10.0/24 via 192.168.1.1 dev eth0`

---

### Ejercicio 27

Elimina la ruta 10.10.10.0/24 añadida en el ejercicio anterior.

**Comando:** `sudo ip route del 10.10.10.0/24`

---

### Ejercicio 28

Si la interfaz eth0 está deshabilitada, ¿qué comando usarías para levantarla?

**Comando:** `sudo ifconfig eth0 up`

---

### Ejercicio 29

¿Qué comando utilizarías para asignar la dirección MAC 02:1A:2B:3C:4D:5E a la interfaz eth0?

**Comando:** `sudo ip link set dev eth0 address 02:1A:2B:3C:4D:5E`

---

### Ejercicio 30

¿Cómo renombrarías la interfaz eth0 para que se llame lan0?

**Comando:** `sudo ip link set eth0 name lan0`