# Margen Retail Moda — publicar en GitHub Pages

App web de cálculo de costos, precios y rentabilidad para compras de moda.
Funciona sin servidor: son archivos estáticos. Una vez publicada tendrás un
enlace público que cualquier persona del equipo puede abrir e instalar en su celular.

## Contenido del paquete

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La aplicación completa (los 4 módulos). Es lo único imprescindible. |
| `manifest.webmanifest` | Permite instalarla como app con nombre e ícono propios. |
| `sw.js` | Hace que funcione sin conexión después de la primera visita. |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | Íconos de la app. |

> Los cuatro archivos deben quedar en la **misma carpeta**, al mismo nivel.

---

## Paso a paso (sin instalar nada, todo desde el navegador)

### 1. Crear la cuenta
Entra a <https://github.com> y crea una cuenta gratuita si aún no tienes.
Confirma el correo antes de seguir.

### 2. Crear el repositorio
1. Arriba a la derecha, botón **+** → **New repository**.
2. **Repository name**: `margen` (en minúsculas, sin espacios ni tildes).
3. Marca **Public**. *GitHub Pages gratis solo funciona con repositorios públicos.*
4. **No** marques "Add a README file".
5. Botón **Create repository**.

### 3. Subir los archivos
1. En la pantalla que aparece, haz clic en **uploading an existing file**
   (o entra a la pestaña **Add file** → **Upload files**).
2. Descomprime el ZIP en tu computadora y arrastra **los archivos sueltos**
   (`index.html`, `manifest.webmanifest`, `sw.js` y los tres `.png`).
   No arrastres la carpeta: deben quedar en la raíz del repositorio.
3. Abajo, en **Commit changes**, escribe `Primera versión` y presiona
   **Commit changes**.

### 4. Activar GitHub Pages
1. Pestaña **Settings** (arriba, dentro del repositorio).
2. Menú lateral izquierdo → **Pages**.
3. En **Source** elige **Deploy from a branch**.
4. En **Branch** elige `main` y carpeta `/ (root)`. Presiona **Save**.
5. Espera entre 1 y 3 minutos y recarga esa misma página: aparecerá un recuadro
   con el mensaje *"Your site is live at…"* y tu enlace.

Tu dirección será:

```
https://TU-USUARIO.github.io/margen/
```

### 5. Instalarla en el celular
Abre ese enlace en el teléfono y:

- **Android (Chrome)**: menú **⋮** → *Instalar aplicación* / *Añadir a pantalla principal*.
- **iPhone (Safari)**: botón **Compartir** → *Añadir a pantalla de inicio*.

Queda con su ícono, se abre a pantalla completa y sigue funcionando sin señal.
En iPhone el paso debe hacerse desde **Safari**; desde Chrome no aparece la opción.

---

## Actualizar la app más adelante

1. Entra al repositorio → **Add file** → **Upload files**.
2. Sube el `index.html` nuevo (sobrescribe el anterior) y confirma con **Commit changes**.
3. Abre `sw.js` en GitHub, presiona el lápiz ✏️ y cambia `margen-v2` por `margen-v3`.
   Eso obliga a los celulares a descargar la versión nueva en lugar de la guardada.
4. Confirma el cambio. En 1–2 minutos el sitio queda actualizado.

## Notas

- Todo el cálculo ocurre en el dispositivo: **no se envía ningún dato a ningún servidor**.
- Los valores que cada persona escribe se guardan solo en su propio teléfono o computadora.
- El repositorio es público, así que cualquiera con el enlace puede abrir la app.
  No coloques dentro del archivo información confidencial (costos reales de proveedores,
  nombres de marcas). Los datos que se escriben al usarla no quedan en el repositorio.
- Si prefieres que el sitio sea privado, GitHub Pages privado requiere plan de pago;
  una alternativa gratuita es Netlify Drop con enlace no listado.

## Alternativa en 30 segundos: Netlify Drop

Si no quieres crear cuenta de GitHub: entra a <https://app.netlify.com/drop>,
arrastra la carpeta completa y obtienes un enlace al instante.
Para conservarlo permanentemente sí pide crear una cuenta gratuita.
