# Sitio personal de Patricia Acetta

Sitio publicado en: **https://pacetta.github.io**
Repositorio: **https://github.com/pacetta/pacetta.github.io**

## Cómo está armado

- Todo el sitio es **un solo archivo**: `index.html`. Ahí está el texto, los estilos (diseño/colores) y la foto de perfil (incrustada directamente en el código, no es un archivo de imagen aparte).
- Es HTML simple: no usa ningún programa ni instalación especial.
- Se publica solo con **GitHub Pages**: cada vez que se sube un cambio a la rama `main`, el sitio se actualiza automáticamente en 1-2 minutos. No hay que hacer nada manual para "subirlo".

## Cómo pedir un cambio

Lo más simple: pedírselo a Claude (en esta misma conversación o en una nueva, mencionando el sitio). Si en algún momento lo edita otra persona a mano, el archivo a tocar es `index.html`.

## Formulario de contacto — Web3Forms

El formulario de la sección "Contacto" manda los mensajes directo a tu email usando un servicio gratuito llamado **Web3Forms**.

**No existe usuario ni contraseña.** Web3Forms no es una cuenta tradicional, funciona así:

1. En su momento ingresaste tu email (`pmacetta@gmail.com`) en **web3forms.com**.
2. Te generaron una **Access Key** (clave de acceso), que es esta:
   ```
   c9ea82f7-ec8d-49ed-9fba-7f57d2723d69
   ```
3. Esa clave está pegada directamente en el código de `index.html` (buscar `access_key`). Es una clave **pública a propósito** — Web3Forms la diseñó para que pueda estar visible en el código de cualquier sitio, no es un dato secreto como una contraseña.
4. Cuando alguien completa el formulario en el sitio y aprieta "Enviar", Web3Forms recibe esa clave, identifica que el mensaje es de tu sitio, y te lo reenvía automáticamente por email a `pmacetta@gmail.com`.

### Si en el futuro necesitás...

- **Recuperar o confirmar la clave**: entrá a web3forms.com, volvé a poner tu email, y te la reenvían al toque.
- **Cambiar a qué email llegan los mensajes**: generar una clave nueva en web3forms.com con el otro email, y reemplazar el valor de `access_key` en `index.html`.
- **Ver el límite de envíos**: el plan gratuito permite 250 mensajes por mes, más que suficiente para un sitio personal. No requiere loguearse a ningún panel para que funcione.
- **Desactivarlo**: borrar el `<form>` de la sección de contacto en `index.html` (igual quedan el email, LinkedIn y ORCID como contacto directo).

## Dónde se configura GitHub Pages

Por si algún día hay que revisarlo: **github.com/pacetta/pacetta.github.io → Settings → Pages**. Tiene que decir "Source: Deploy from a branch", rama `main`, carpeta `/ (root)`.
