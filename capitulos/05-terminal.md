# Terminal y Tmux

[Alacritty](https://alacritty.org/) es la terminal por defecto de Omarchy. Es rápida, hermosa y compatible incluso con computadoras antiguas. Sin embargo, no soporta pestañas nativas, divisiones ni renderizado de imágenes.

Si usas Tmux, puede que no te moleste, pero si no, también soportamos completamente *Ghostty* y *Kitty* como opciones. Elige tu preferencia bajo *Instalar > Terminal* en el menú de Omarchy.

Inicias una nueva terminal con `Super + Return`. (Este atajo apuntará automáticamente a la Terminal que hayas instalado via *Instalar > Terminal*).

## Tmux

Tmux proporciona una interfaz consistente y programable para paneles, ventanas (aka pestañas) y sesiones reanudables sin importar tu terminal. Incluso funciona en hosts remotos, así que cuando estés conectándote por SSH a un servidor, puedes usar el mismo enfoque.

Inicias una nueva sesión Tmux en una terminal fresca con `Super + Alt + Return`, y porque Tmux es un proceso persistente, puedes reanudar tu sesión incluso si cierras esa terminal. Solo presiona `Ctrl + Space` (llamada la tecla prefijo) luego `s` para ver todas tus sesiones activas.

Omarchy viene con una configuración de Tmux optimizada ergonómicamente, que tiene muchos atajos para aprender, así que mantén [la guía rápida](./04-atajos.md#tmux) a mano.

## Funciones de layout de Tmux

Porque Tmux es programable, podemos usar funciones para crear layouts. Omarchy viene con tres funciones diferentes para layouts comunes de desarrollo.

`tdl [agente]` inicia una interfaz estilo IDE de tres vías con el `$EDITOR` a la izquierda, tu agente AI elegido a la derecha (como `c` para opencode o `cx` para Claude o `codex` para OpenAI), y luego una terminal abajo.

Entonces `tdl c` iniciaría esto:

![Layout tdl con Claude](https://jricardo88.github.io/omarchy-manual-es/img/tmux-tdl-x-dxhZe9.png)

También puedes iniciar un segundo agente con `tdl c cx` (opencode + claude):

![Layout tdl con dos agentes](https://jricardo88.github.io/omarchy-manual-es/img/tmux-tdl2-x-5FoPqh.png)

También puedes iniciar esta configuración de layout para cada subdirectorio en el directorio actual usando `tdlm [agente]`, luego navegas usando `alt + 1/2/3/5/6/...`:

![Layout tdlm](https://jricardo88.github.io/omarchy-manual-es/img/tdlm-x-RPg6sr.png)

Finalmente, puedes iniciar un enjambre de agentes usando `tsl [paneles] [comando]`. Entonces `tsl 4 c` te dará una cuadrícula de cuatro vías de agentes opencode:

![Layout tsl con 4 paneles](https://jricardo88.github.io/omarchy-manual-es/img/tsl-x-SFzDeo.png)

---

← [Anterior: Atajos de teclado](04-atajos.md) | [Índice](../README.md) | [Siguiente: Neovim →](06-neovim.md)
