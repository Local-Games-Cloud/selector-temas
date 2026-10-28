# Discord Developer

Plugin de código para Local Games: mientras usas la biblioteca o juegas, tu
**perfil de Discord** muestra la actividad en tiempo real (con cronómetro).

## Cómo se usa

1. Sube este repositorio a https://github.com/Local-Games-Cloud
2. En Local Games → **Plugins**, pulsa **Descargar plugin**.
3. Listo: al instalarlo se añade la sección **Developer** en el sidebar y la
   actividad se publica sola (con Discord abierto).

En **Developer** puedes:

- **Encender o apagar** la actividad con el interruptor.
- Elegir **Automática** (biblioteca / juego) o **Personalizada** y escribir tus
  propias dos líneas de texto.
- Ver el estado: si falta el `client_id`, la sección te avisa.

## Importante: el client_id de Discord

Rich Presence necesita una **aplicación registrada** en Discord (es gratis y se
hace una sola vez):

1. Abre https://discord.com/developers/applications → **New Application**.
2. Copia la **Application ID** (General Information).
3. Pégala en el campo `discordClientId` de `plugin.json`:

```json
"discord": true,
"discordClientId": "123456789012345678"
```

4. Sube el repositorio de nuevo. Todos los usuarios que instalen el plugin ya
   no tienen que configurar nada.

## El logo de la actividad

En **Rich Presence → Recursos artísticos** del portal se sube la imagen que
aparece al lado de la actividad (recomendado 1024×1024, PNG/JPG, máx. 10 MB):

1. Botón **Añadir imagen(es)** → elegir el archivo → ponerle una **clave**.
2. *Save Changes*. Ojo: la clave no se puede editar después, solo borrar y
   volver a subir.
3. Esa misma clave va en `plugin.json`:

```json
"discordLargeImage": "local_games"
```

Si el campo queda vacío, la actividad se publica sin imagen.

## Archivos

- `plugin.json` — información del plugin (obligatorio); `discord: true` es lo que
  hace que el launcher añada la sección Developer, `discordClientId` da la
  actividad a Discord y `discordLargeImage` elija el logo.
- `logo.png` — logo del plugin (obligatorio).
- `plugin-comprimido.zip` — el plugin completo, con el nombre que exige la app.

## Notas

- La conexión con Discord la hace el propio launcher (sin dependencias): usa el
  socket local `\\.\pipe\discord-ipc-0` y se reintenta solo si Discord está
  cerrado.
- Si quitas el plugin, la sección Developer desaparece y la actividad se apaga.
