# Facturas Boutique

## Ejecutar
1. Instala Node.js (https://nodejs.org).
2. En esta carpeta: `node server.js` (o `npm start`).
3. Abre http://localhost:3000

## Importante para el iPhone
- La cámara (escáner) en iPhone SOLO funciona con HTTPS. Con http://IP-local el escáner no abrirá.
- Opción recomendada: sube la carpeta `public` a un hosting gratuito con HTTPS
  (Netlify Drop, Vercel, GitHub Pages o Cloudflare Pages) y abre ese enlace en Safari.
- Opción local: crea un certificado y reinicia el servidor (arranca en HTTPS solo):
  `openssl req -x509 -newkey rsa:2048 -nodes -keyout key.pem -out cert.pem -days 365 -subj "/CN=localhost"`
  (Safari mostrará una advertencia de certificado que debes aceptar; puede no ser suficiente para la cámara.)
- Luego: Compartir > "Añadir a pantalla de inicio".

## Datos
- Sin iniciar sesión, los datos se guardan en el navegador de este dispositivo.
- Pulsa "Vincular con Google" para sincronizar productos, fotos y facturas con Firebase. Usa la misma cuenta de Google en tus dispositivos.
- Al vincular por primera vez, los datos locales se combinan con los de tu cuenta de Firebase.
- Haz respaldos con los botones CSV del Historial (abren en Excel o Google Sheets).
- Los datos de cada cuenta están protegidos por reglas de Firestore; no compartas tus credenciales.
- Las librerías (códigos de barras, PDF, escáner) se cargan desde cdnjs.cloudflare.com: se necesita internet la primera vez.
