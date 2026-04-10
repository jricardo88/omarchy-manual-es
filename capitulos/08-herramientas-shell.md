# Herramientas shell

Además de las herramientas estándar de Linux, Omarchy también viene con un montón de herramientas shell mejoradas. Aquí están las principales.

## fzf

[fzf](https://junegunn.github.io/fzf/) te da búsqueda difusa de archivos via el alias `ff`. Ve a cualquier directorio, escribe `ff`, y podrás encontrar de forma difusa tu camino a cualquier archivo en ese árbol, mientras ves una previsualización de los archivos a los que te estás acercando en el lado derecho.

Puedes usar `Ctrl + R` para usar fzf para buscar de forma difusa a través de tu historial de comandos.

Esta herramienta también es usada por Neovim cuando escribes `Space Space`.

El manual completo está disponible via `man fzf`.

## Zoxide

[Zoxide](https://github.com/ajeetdsouza/zoxide) es un reemplazo para cd. Recuerda los directorios en los que has estado, así que puedes saltar a ellos más fácilmente la próxima vez. Digamos que haces `cd ~/.local/share/omarchy` una vez. La próxima vez, puedes simplemente hacer `cd omarchy` (o incluso solo `cd oma`), y Zoxide te llevará directamente ahí.

El manual completo está disponible via `man zoxide`.

## ripgrep

[ripgrep](https://github.com/BurntSushi/ripgrep) busca en el contenido de archivos usando `rg <patrón> <ruta>`, como `rg Controller app/` para encontrar todas las menciones de `Controller` en el directorio app.

Esta herramienta también es usada por Neovim cuando escribes `Space S G`.

El manual completo está disponible via `man rg`.

## eza

[eza](https://eza.rocks/) es un reemplazo para ls. Te da listados de directorio con más información, color e iconos. Por defecto, eza ha sido aliasado como `ls`. También puedes usar `lt` para obtener un listado de dos niveles de anidamiento. `lsa` te da un listado incluyendo archivos ocultos. Y `lta` un listado anidado con archivos ocultos.

El manual completo está disponible via `man eza`.

## fd

[fd](https://github.com/sharkdp/fd) es un reemplazo más fácil de usar para `find`. Usa `fd persona.rb` para encontrar un archivo llamado `persona.rb` dentro del árbol actual. `fd persona.rb /` buscará en todo el sistema de archivos. `fd persona.rb / -H` busca en todo el sistema de archivos, incluyendo directorios ocultos.

El manual completo está disponible via `man fd`.

## try

[try](https://github.com/tobi/try) facilita administrar experimentos de programación con directorios con fecha. Todos los experimentos viven en `~/Work/tries` y puedes accederlos via `try`.

---

# Funciones de shell

Omarchy viene con un conjunto de funciones de shell para simplificar tareas comunes y encapsular llamadas de parámetros complejas.

## Compresión

- `compress [archivo/dir]`: Crear un archivo tar.gz del archivo/dir.
- `decompress [archivo.tar.gz]`: Expandir un archivo tar.gz.

## Discos

- `iso2sd [imagen.iso]`: Crear una unidad booteable en una tarjeta SD usando la imagen iso referenciada y seleccionando la unidad de forma interactiva.
- `format-drive`: Seleccionar un disco entero para formatear con una sola partición exFAT (que funciona en Windows y macOS también). ¡Cuidado!

## Transcodificación

- `img2jpg`: Convertir cualquier imagen a un JPG de casi plena calidad.
- `img2jpg-small`: Convertir cualquier imagen a un JPG de casi plena calidad de 1080p de ancho.
- `img2jpg-medium`: Convertir cualquier imagen a un JPG de casi plena calidad de 1800p de ancho.
- `img2png`: Convertir cualquier imagen a un PNG comprimido pero sin pérdida.
- `transcode-video-1080p`: Transcodificar un video a un MP4 1080p de buen balance.
- `transcode-video-4K`: Transcodificar un video a un MP4 4K de buen balance.

## Reenvío de puertos SSH

Ideal para hacer desarrollo web con privilegios de contexto seguro de localhost contra un servidor remoto.

- `fip`: Reenviar uno o más puertos desde un host remoto a localhost via SSH.
- `dip`: Desconectar uno o más puertos reenviados.
- `lip`: Listar todos los reenvíos de puertos SSH activos.

Digamos que inicias un servidor de desarrollo en el puerto `3000` en una máquina accesible como `nyc-dev`, entonces puedes ejecutar `fip nyc-dev 3000` para reenviar ese puerto, así `localhost:3000` realmente alcanza `nyc-dev:3000`, pero sin necesidad de certificados SSL para establecer el contexto seguro necesario para probar websockets o similares.
