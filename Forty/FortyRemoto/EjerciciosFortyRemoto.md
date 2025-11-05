# Ejercicios Forty Remoto

### Ejercicio 1

Sube al remoto los ficheros de tu repositorio local.

```bash
git remote add origin https://github.com/Hugoo-11/forty_remoto.git
git branch -M main
git push -u origin main

```

---

### Ejercicio 2

En local, crea una rama 'feature-head'. Cambia el título en la sección head de index.html, borra los comentarios del head o previos también.

Confirma y sube los cambios al remoto.

```bash
git checkout -b feature-head
git add index.html
git commit -m "Modificado el titulo del index.html"
git push -u origin feature-head

```

---

### Ejercicio 3

En remoto, crea una rama 'feature-articulo'. Duplica la página generic, nómbrala como articulo.html y añade como contenido un artículo sobre Git.

Confirma los cambios y realiza un commit. Muestra los commits del repositorio tal como se ven en GitHub.

```
Entrar en el repositorio y crear la rama feature-articulo.
Crear un archivo llamado articulo.html y meterle dentro lo mismo que hay en generic.html
y escribir un artículo sobre GIT. Pulsa commit changes.

```

---

### Ejercicio 4

En el repositorio local examina los cambios. Actualiza el repositorio con el remoto.

Fusiona en 'main' las dos ramas 'feature'. Crea la etiqueta 'v2.0'.

Muestra los logs, commits, etiquetas y ramas actuales, en local y en remoto.

```bash
git fetch --all
git checkout main
git pull origin main
git merge --no-ff origin/feature-head -m "Merge feature-head a main"
git merge --no-ff origin/feature-articulo -m "Merge feature-articulo into main"
git tag v2.0
git push origin main --follow-tags
git log --oneline --graph --decorate --all

```

![Captura de pantalla 2025-10-29 174132.png](Captura_de_pantalla_2025-10-29_174132.png)

---

### Ejercicio 5

En tu copia local, crea una rama nueva. En la rama nueva, cambia los enlaces de la página index.html

para que apunten correctamente a la nueva página articulo.html. Confirma los cambios.

```bash
git checkout -b rama_links
# editar los enlaces dentro del archivo index.html
git add index.html
git commit -m "Cambiado los enlaces en index.html"

```

---

### Ejercicio 6

Muestra los logs de forma que se vean las ramas en tu copia local.

```bash
git log --oneline --graph --decorate --all

```

![Captura de pantalla 2025-10-29 175231.png](Captura_de_pantalla_2025-10-29_175231.png)

---

### Ejercicio 7

Te gusta el resultado de los cambios. Incorpora los cambios de la rama nueva a la principal.

```bash
git checkout main
git merge --no-ff rama_links -m "Fusionado la rama_links con todo"

```

---

### Ejercicio 8

Sube los cambios al remoto borrando la rama nueva, si es necesario.

Comprueba primero con un comando en local las ramas que hay en el repositorio remoto.

```bash
git branch -r
# Solo la tenia creada en local, no subi nada con lo cual hacemos esto:
git push origin main
git branch -d rama_links

```

---

### Ejercicio 9

Muestra en local los cambios en el archivo index.html entre la versión actual y la anterior.

```bash
git diff HEAD~1 -- index.html

```

![Captura de pantalla 2025-10-29 180223.png](Captura_de_pantalla_2025-10-29_180223.png)

---

### Ejercicio 10

En el repositorio en GitHub, navega hasta el archivo index.html y selecciona la opción **History**.

![Captura de pantalla 2025-10-29 180457.png](Captura_de_pantalla_2025-10-29_180457.png)