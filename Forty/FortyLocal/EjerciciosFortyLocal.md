# Ejercicios Forty Local

### Ejercicio 1

Inicializa un nuevo repositorio Git en una carpeta llamada "forty" y agrega los archivos proporcionados en el aula virtual.

```bash
mkdir forty
cd forty
```

![image.png](image.png)

---

### Ejercicio 2

Renombra la rama master a main.

```bash
git init
git branch -M main
```

![image.png](image%201.png)

---

### Ejercicio 3

Haz que los ficheros README.txt, LICENSE.txt y passwords.txt sean ignorados por el control de versiones.

```bash
notepad .gitignore
# Meter lo siguiente dentro
README.txt
LICENSE.txt
passwords.txt
```

![image.png](image%202.png)

---

### Ejercicio 4

Crea el archivo passwords.txt. Comprueba que el control de versiones lo ignora.

```bash
echo "mis contraseñas" > passwords.txt
git status
```

![image.png](image%203.png)

---

### Ejercicio 5

Crea una rama llamada "feature-content". Muévete a esa rama. Cambia, en la línea 3477, el font-size por 1.5em en el archivo main.css.

Confirma cambios y haz commit. Muestra los logs de la forma más gráfica posible.

```bash
git checkout -b feature-content
cd assets
cd css
notepad main.css
# font-size: 1.5em;
git add main.css
git commit -m "Cambio de font-size a 1.5em en main.css"
git log --graph --oneline --all

```

![image.png](image%204.png)

---

### Ejercicio 6

Elimina el archivo "passwords.txt" en la carpeta forty. Verifica el estado del repositorio. ¿Hay cambios pendientes?

```bash
rm password.txt
git status
```

![image.png](image%205.png)

---

### Ejercicio 7

Crea un nuevo archivo llamado "about.html", partiendo del archivo generic.html, y agrégalo al repositorio.

Haz un nuevo commit.

```bash
cp generic.html about.html
git add about.html
git commit -m "Añadido about.html a partir de generic.html"
```

![image.png](image%206.png)

---

### Ejercicio 8

Cambia a la rama main. Examina los logs del repositorio de forma gráfica.

```bash
git checkout main
git log --graph --oneline --all

```

---

### Ejercicio 9

Modifica algo en el archivo generic.html, comprueba que hay cambios, y realiza otro commit.

Examina los logs del repositorio de forma gráfica.

```bash
notepad generic.html
git add generic.html
git commit -m "Cambio pequeño en generic.html"
```

![image.png](image%207.png)

---

### Ejercicio 10

Modifica algo en el fichero elements.html. Confirma los cambios, pero no hagas commit.

```bash
notepad elements.html
# Modificar lo que quieras

```

---

### Ejercicio 11

Mira las diferencias de elements.html. Los cambios no nos gustan, deshaz los cambios de elements.html.

Comprueba que no hay cambios pendientes.

```bash
git diff --staged elements.html
git restore --staged elements.html
git restore elements.html
git status

```

---

### Ejercicio 12

Muestra las diferencias entre dos ramas.

```bash
git diff main..feature-content

```

![image.png](image%208.png)

---

### Ejercicio 13

Fusiona la rama "feature-content" con la rama principal (main).

Muestra los logs del repositorio de una forma gráfica y completa.

```bash
git merge feature-content
git log --graph --oneline --all

```

---

### Ejercicio 14

Crea una nueva rama llamada "hotfix" y en ella, corrige un error crítico en el archivo "index.html"

(por ejemplo, añade el enlace a la nueva página about.html).

```bash
git checkout -b hotfix
git add index.html
git commit -m "Hotfix: añadido enlace a about.html en index.html"

```

![image.png](image%209.png)

---

### Ejercicio 15

Fusiona la rama "hotfix" con la rama principal y verifica el historial de commits de forma que se vean todas las ramas gráficamente.

¿Borrarías la rama hotfix? ¿En qué caso? ¿Cómo?

```bash
git checkout main
git merge hotfix
git log --graph --oneline --all
```

![image.png](image%2010.png)

---

### Ejercicio 16

Muestra el historial de cambios limitado a los últimos 3 commits.

```bash
git log -3

```

![image.png](image%2011.png)

---

### Ejercicio 17

Etiqueta el commit actual como "v1.0" y muestra las etiquetas existentes.

```bash
git tag v1.0
git tag
git show v1.0

```

![image.png](image%2012.png)