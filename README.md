# Selector de temas

Plugin de tema para Local Games: cambia el tema de la interfaz entre
**Oscuro**, **Claro**, **Azul**, **Verde** o el **predeterminado del sistema**.

## Cómo se usa

1. Sube este repositorio a https://github.com/Local-Games-Cloud
2. En Local Games → **Plugins → Temas**, pulsa **Descargar plugin**.
3. Activa el interruptor del plugin: aparecerán los **chips** con las variantes.
4. Un clic en un chip cambia el tema al instante (sin reiniciar).
   La variante «Predeterminado del sistema» sigue el esquema claro/oscuro de Windows.

## Variantes

- `dark.css` — Oscuro (paleta por defecto del launcher)
- `light.css` — Claro
- `system.css` — Predeterminado del sistema (claro/oscuro según Windows)
- `blue.css` — Azul
- `green.css` — Verde

## Archivos

- `plugin.json` — información del plugin con la lista de `variants` (obligatorio)
- `logo.png` — logo del plugin (obligatorio)
- `*.css` — las variantes (dentro de `plugin-comprimido.zip`)
- `plugin-comprimido.zip` — el plugin completo, con el nombre que exige la app
