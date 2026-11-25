# El Rosco de la Energía

Juego tipo rosco (Pasapalabra) sobre la energía: energías renovables, no renovables y energías limpias, para 4.º de Educación Primaria.
Incluye una versión normal y una versión con apoyos visuales (TEA). No necesita instalar nada ni usar servidor.

## Cómo usarlo

1. Descomprime la carpeta.
2. Abre `index.html` en el navegador (doble clic).
3. Para abrir directamente la versión con apoyos visuales, usa `index.html#tea` (por ejemplo, creando un acceso directo a esa dirección).

Funciona sin internet. Si hay conexión, el navegador descarga las tipografías Fredoka y Nunito de Google Fonts. Sin conexión usa las tipografías del sistema y el juego funciona igual.

## Qué hay en la carpeta

| Archivo | Para qué sirve |
|---|---|
| `index.html` | Estructura de la página |
| `css/styles.css` | Colores, tipografías y diseño. Los colores están al principio, en variables (`--leaf`, `--water`...), con una paleta clara y otra oscura |
| `js/game.js` | Lógica del juego y todos los contenidos |
| `img/cabecera-claro.svg`, `img/cabecera-oscuro.svg` | Ilustración de la cabecera (paisaje con aerogeneradores, casa con placas solares y campo de paneles). Se usa una u otra según el modo claro u oscuro del dispositivo |
| `img/favicon.svg` | Icono de la pestaña |

Los pictogramas de la versión con apoyos visuales son emojis, que se ven distinto según el dispositivo. Para usar otros pictogramas (por ejemplo, de ARASAAC), se pueden sustituir en `js/game.js`.

## Cómo cambiar preguntas y pruebas

Todo está en `js/game.js`, al principio:

- `ITEMS` es la lista de letras de la versión normal. Cada letra es una pregunta (`type:'q'`, con `clue`, `answers` y `fact`) o una prueba comodín (`type:'c'`, con `name`, `text`, `seconds` y `fact`). `answers` admite varias formas de escribir la respuesta.
- `TEA` es la lista de la versión con apoyos visuales, con la misma letra como clave. En las preguntas, `opts[0]` es siempre la respuesta correcta y las otras dos son distractores. En las pruebas, `steps` son los pasos con pictograma.
- Las letras tienen que estar ordenadas como se quiere ver en el rosco. El número de letras se ajusta solo.

## Cómo compartirlo

- Para usarlo sin conexión, reparte la carpeta (USB, plataforma del centro...) y abre `index.html`.
- Para compartirlo con un enlace o un código QR, sube la carpeta completa a cualquier alojamiento web y crea el QR con esa dirección.
- Algunos navegadores de tablet no abren bien archivos HTML guardados en local. Si pasa, es mejor alojarlo en una web.
