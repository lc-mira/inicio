# Mira — Landing page

Sitio estático (HTML + CSS + JS, sin dependencias) con la landing de presentación de Mira y la política de tratamiento de datos.

## Archivos

```
index.html        → Landing principal
privacidad.html    → Política de tratamiento de datos personales
img/
  mira-wordmark.png   → Logo "mira" (para el menú)
  mira-completo.png   → Logo "mira · leads calificados" (para el pie de página)
```

## Pendientes antes de publicar

- [ ] **Fecha de la política**: en `privacidad.html`, busca `[FECHA DE PUBLICACIÓN]` y reemplázalo por la fecha real.
- [ ] Revisa la frase de `privacidad.html` sobre dónde se almacenan los datos ("Google Drive u otros repositorios") — según la arquitectura del sistema, los leads en realidad se guardan en **Google Sheets**; ajústala si quieres que sea exacta.
- [ ] El número de WhatsApp (573164854961) ya está enlazado en el botón "Escríbenos por WhatsApp" de `index.html`.

## Publicar en GitHub Pages (gratis)

1. Crea un repositorio nuevo en GitHub (puede ser público o privado; GitHub Pages funciona con ambos si tienes plan Pro, o público si es gratuito).
2. Sube estos archivos a la raíz del repo, conservando la carpeta `img/`:
   ```bash
   cd mira-landing
   git init
   git add .
   git commit -m "Landing de Mira"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/TU-REPO.git
   git push -u origin main
   ```
   (O arrástralos directamente desde la interfaz web de GitHub con "Add file → Upload files".)
3. En el repo, ve a **Settings → Pages**.
4. En "Source", elige **Deploy from a branch**, rama `main`, carpeta `/ (root)`. Guarda.
5. GitHub te da una URL del tipo `https://TU-USUARIO.github.io/TU-REPO/` en 1–2 minutos.

## Dominio propio (opcional)

Si quieres usar un dominio como `www.miralead.com` en vez de la URL de GitHub:
1. En tu proveedor de dominio, crea un registro CNAME apuntando `www` a `TU-USUARIO.github.io`.
2. En **Settings → Pages → Custom domain**, escribe tu dominio y guarda (esto crea un archivo `CNAME` en el repo).
3. Activa "Enforce HTTPS" cuando GitHub lo habilite (puede tardar unos minutos).

## Notas técnicas

- No requiere build ni dependencias: son archivos estáticos puros.
- El selector de precios Mensual/Anual en la sección de Planes funciona con JavaScript simple, sin librerías externas.
- Las fuentes (Sora, Inter, JetBrains Mono) se cargan desde Google Fonts vía CDN.
