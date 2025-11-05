# Ejercicios Linux Typora

### 1- ¿En qué directorio se encuentran los ficheros de configuración del sistema? # Ejercicios Linux

```bash
% /etc

```

### 2- Para entrar en un sistema Linux hace falta a) nombre de usuario, contraseña y dirección IP, b) nombre de usuario y contraseña o c) únicamente una contraseña. # Ejercicios Linux

```bash
b) Nombre de usuario y contraseña

```

### 3- Muestra el contenido del directorio actual. # Ejercicios Linux

```bash
$ ls
```

![image.png](image.png)

### 4- Muestra el contenido del directorio que está justo a un nivel superior # Ejercicios Linux

```bash
$ ls..

```

### 5- ¿En qué día de la semana naciste?, utiliza la instrucción cal para averiguarlo. # Ejercicios Linux

```bash
$ cal 07 2004

```

![image.png](image%201.png)

### 6- Muestra los archivos del directorio /bin # Ejercicios Linux

```bash

ls/bin
```

### 7- Suponiendo que te encuentras en tu directorio personal (/home/nombre), muestra un listado del contenido de /usr/bin a) con una sola línea de comando, b) moviéndote paso a paso por los directorios y c) con dos líneas de comandos. # Ejercicios Linux

```bash
a) ls /usr/bin
b) cd /usr
   cd /bin
c) cd /usr/bin
   ls

```

![image.png](image%202.png)

### 8- Muestra todos los archivos que hay en /etc y todos los que hay dentro de cada subdirectorio, de forma recursiva (con un solo comando) # Ejercicios Linux

```bash
ls -R /etc

```

### 9- Muestra todos los archivos del directorio /usr/X11R6/bin ordenados por tamaño (de mayor a menor). Sólo debe aparecer el nombre de cada fichero, sin ninguna otra información adicional. # Ejercicios Linux

```bash
cd /usr/bin
ls -S
```

![image.png](image%203.png)

### 10- Muestra todos los archivos del directorio /etc ordenados por tamaño (de mayor a menor) junto con el resto de características, es decir, permisos, tamaño, fechas de la última modificación, etc. El tamaño de cada fichero debe aparecer en un formato “legible”, o sea, expresado en Kb, Mb, etc # Ejercicios Linux

```bash
ls -lSh /etc

```

![image.png](image%204.png)

### 11- Muestra todos los archivos del directorio /bin ordenados por tamaño (de menor a mayor). Sólo debe aparecer el tamaño y el nombre de cada fichero, sin ninguna otra información adicional. El tamaño de cada fichero debe aparecer en un formato “legible”, o sea, expresado en Kb, Mb, etc. # Ejercicios Linux

```bash
ls -lhS /bin | tac

```

### 12- Muestra el contenido del directorio raíz utilizando como argumento de ls una ruta absoluta. # Ejercicios Linux

```bash
ls /
```

![image.png](image%205.png)

### 13- Muestra el contenido del directorio raíz utilizando como argumento de ls una ruta relativa. Suponemos que el directorio actual es /home/elena/documentos. # Ejercicios Linux

```bash
ls ././.

```

### 14- Crea el directorio gastos dentro del directorio personal. # Ejercicios Linux

```bash

mkdir ~/gastos
```

![image.png](image%206.png)

### 15- ¿Qué sucede si se intenta crear un directorio dentro de /etc? # Ejercicios Linux

```bash

sudo mkdir /etc/prueba
```

### 16- Muestra el contenido del fichero /etc/fstab # Ejercicios Linux

```bash
ls /etc/fstab

```

### 17- Muestra las 10 primeras líneas del fichero /etc/bash.bashrc # Ejercicios Linux

```bash
head -n 10 /etc/bash.bashrc

```

### 18- Crea la siguiente estructura de directorios dentro del directorio de trabajo personal: # Ejercicios Linux

```bash
mkdir -p ~/documentos/trabajos/musica
```

![image.png](image%207.png)

### 19- Crea un fichero vacío dentro del directorio musica, con nombre estilos_favoritos.txt # Ejercicios Linux

```bash
touch estilos_favoritos.txt

```

![image.png](image%208.png)

### 20- Utiliza tu editor preferido para abrir el fichero estilos_favoritos.txt e introduce los estilos de música que más te gusten. Guarda los cambios y sal. # Ejercicios Linux

```bash

nano estilos_favoritos.txt

```

![image.png](image%209.png)

### 21- Muestra todo el contenido de estilos_favoritos.txt # Ejercicios Linux

```bash
cat estilos_favoritos.txt
```

![image.png](image%2010.png)

### 22- Muestra las 3 primeras líneas de estilos_favoritos.txt # Ejercicios Linux

```bash
head -n 3 estilos_favoritos.txt
```

![image.png](image%2011.png)

### 23- Muestra la última línea de estilos_favoritos.txt # Ejercicios Linux

```bash
tail -n 1 estilos_favoritos.txt

```

![image.png](image%2012.png)

### 24- Muestra todo el contenido del fichero estilos_favoritos.txt excepto la primera línea. Se supone que no sabemos de antemano el número de líneas del fichero # Ejercicios Linux

```bash
tail -n +2 estilos_favoritos.txt
```

![image.png](image%2013.png)