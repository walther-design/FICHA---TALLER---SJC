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

## Roles

- **Administrador** (`walther@sanjoseconcretos.com`): carga e importa la flota, edita y elimina móviles, cambia los ítems del checklist y los ajustes de avisos, elimina fichas (abiertas o cerradas), reabre fichas cerradas y maneja los respaldos.
- **Taller** (cualquier otro usuario): solo crea, completa, firma y cierra fichas (no puede reabrir ni borrar), saca fotos, marca móviles en taller y sigue las alertas.

El email del administrador está en `firestore.rules` (función `esAdmin`) y, opcionalmente, en `config.js` como `window.ADMIN_EMAILS = [...]`. Si se cambia, hay que cambiarlo en los dos y volver a publicar las reglas.
