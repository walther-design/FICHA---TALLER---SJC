# Ficha de Taller SJC

App para tablet y celular que reemplaza la ficha de control de taller en papel de la flota de SJC.

- Se instala desde el navegador (Android: menú ⋮ → "Instalar app"; iPhone/iPad: Compartir → "Agregar a inicio").
- Funciona sin señal y sincroniza cuando vuelve la conexión.
- Datos compartidos en Firebase (Firestore + inicio de sesión con correo y contraseña).

## Archivos

- `index.html`: la app completa.
- `config.js`: datos del proyecto Firebase.
- `sw.js`: guarda la app en el equipo para usarla sin internet.
- `firestore.rules`: reglas de seguridad para pegar en Firestore → Reglas.
