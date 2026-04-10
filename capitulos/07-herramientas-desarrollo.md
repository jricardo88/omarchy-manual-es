# Herramientas de desarrollo

## Editores alternativos

Omarchy viene con [Neovim](https://neovim.io/) por defecto, pero si quieres algo un poco más mainstream y familiar, puedes ejecutar el Menú de Omarchy (`Super + Alt + Space`) y ver las opciones bajo *Instalar > Editor*. Tenemos VSCode, Cursor, Zed, Sublime Text y Helix listados ahí. Si no encuentras lo que buscas, revisa *Instalar > Paquete* y ve si no está en un paquete de Arch (y si no, prueba *Instalar > AUR* para revisar el AUR).

Se ofrece coincidencia de temas para `VSCode`, `Cursor` y `VSCodium`.

Puedes configurar el editor predeterminado del sistema bajo `Configuración > Predeterminados`. Eso abrirá el archivo de predeterminados de UWSM, que controla tanto el editor como la terminal. Después de guardar tu cambio, tienes que reiniciar Hyprland para que surta efecto (`Super + Esc`).

## Entorno

Omarchy soporta configurar todo un conjunto de entornos de desarrollo a través de la sección *Instalar > Desarrollo* del Menú de Omarchy (`Super + Alt + Space`). Por supuesto encontrarás *Ruby on Rails*, pero también los tres mayores runtimes para JavaScript (Node.js, bun, Deno), así como frameworks populares de PHP como Laravel y Symfony. Ah, y también está .NET, OCaml, Zig y Elixir. ¡Es una selección muy amplia!

La mayoría de estos entornos están manejados por [Mise](https://mise.jdx.dev/). Es una herramienta que te permite instalar y ejecutar múltiples versiones de un lenguaje de programación en la misma máquina. Es como rbenv o rvm para Ruby o virtualenv para Python, pero funciona para un montón de entornos diferentes.

Para instalar, digamos, Ruby, ejecutarías `mise use -g ruby`, que instalará Ruby y lo establecerá como el predeterminado global. O, si tu proyecto tiene un archivo .ruby-version, puedes simplemente ejecutar `mise i` en la raíz de ese proyecto.

## Docker

[Docker](https://www.docker.com/) apenas necesita presentación. Permite ejecutar contenedores aislados, y Omarchy instala todo lo necesario para ejecutarlo bien. Esto incluye Docker mismo, [Docker Compose](https://docs.docker.com/compose/) y los cambios de grupo de usuario necesarios para que puedas ejecutar Docker como usuario normal y no como root.

Recuerda revisar el comando Lazydocker para administrar tus contenedores en una cool TUI usando `Super + Shift + D`.

Puedes configurar las bases de datos comunes para desarrollo local en Docker usando *Instalar > Desarrollo > Docker DB* en el menú de Omarchy.

## GitHub CLI

[La CLI de GitHub](https://cli.github.com/) te permite autenticarte con tu cuenta de GitHub y clonar repositorios privados usándola. Para autenticarte, ejecuta `gh auth login`. Luego puedes clonar repositorios privados usando `gh repo clone org/repo`.

También puedes realizar un montón de otras operaciones de GitHub usando este comando. Solo ejecuta `gh` para ver todo lo que es posible.

---

← [Anterior: Neovim](06-neovim.md) | [Índice](../README.md) | [Siguiente: Herramientas shell →](08-herramientas-shell.md)
