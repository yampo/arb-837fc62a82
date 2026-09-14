# Publicar en GitHub Pages

Todo está listo. Lo único que no puedo hacer yo es **crear el repositorio**: la API
de GitHub está bloqueada desde esta sesión y en tu Chrome no estás logueado en
GitHub (y no puedo escribir contraseñas). El resto sí.

## Paso 1 — crear el repo vacío (30 segundos, lo hacés vos)

1. https://github.com/new
2. Nombre: **arb-837fc62a82**  (o el que prefieras)
3. Visibilidad: **Public**
4. **No** marques "Add a README", ni .gitignore, ni licencia — tiene que quedar vacío
5. Create repository

## Paso 2 — avisame y yo subo todo

Con el repo creado, yo hago el push desde acá: git sí tiene salida, lo comprobé.

Si preferís hacerlo vos:

```bash
cd <carpeta-descargada>
git init && git add -A && git commit -m "Árbol genealógico Garicoits"
git branch -M main
git remote add origin https://github.com/yampo/arb-837fc62a82.git
git push -u origin main
```

## Paso 3 — activar Pages (lo hacés vos)

Settings → Pages → Source: **Deploy from a branch**, rama `main`, carpeta `/ (root)`.
En un minuto queda en `https://yampo.github.io/arb-837fc62a82/`

## Sobre el nombre difícil de adivinar

Sirve para que nadie llegue por casualidad a la URL, y le agregué dos capas más:
un `robots.txt` que pide a los buscadores no indexar, y una etiqueta `noindex` en
la página. Con eso no debería aparecer en Google.

**Pero hay algo que el nombre no resuelve:** un repositorio público aparece
listado en tu perfil, en github.com/yampo. Cualquiera que mire tu perfil lo ve,
se llame como se llame. Si lo que querés es que no sea descubrible, las opciones
reales son:

- **Repo privado sin Pages**: lo ves y compartís el archivo, pero no hay web navegable.
- **GitHub Pro** (pago): permite Pages desde repositorio privado, con la página
  accesible solo para quien tenga permiso.
- **El enlace del artefacto de Claude**: es privado por defecto, se comparte con
  quien vos quieras y se actualiza solo cuando yo publico una versión nueva. Para
  compartirlo con tu padre, honestamente, es mejor que GitHub Pages.
