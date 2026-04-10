# Neovim

[Neovim](https://neovim.io/) es una implementación moderna del [editor vi](https://en.wikipedia.org/wiki/Vi_(text_editor)) creado por Bill Joy en 1976. Es un editor modal donde el modo de inserción y el modo comando están separados, y es un poco de superpoder una vez que aprendes incluso solo un subconjunto del increíble conjunto de comandos de teclado. ¡Pero también tiene una curva de aprendizaje considerable!

Si eres totalmente nuevo en la edición estilo vim, te recomiendo ver [ThePrimeagen's Vim As Your Editor series](https://www.youtube.com/watch?v=X6AR2RMB5tE&list=PLm323Lc7iSW_wuxqmKx_xxNtJC_hJbQ7R) en YouTube. Eso te enseñará lo básico. Solo ten en cuenta que a diferencia de editores similares más mainstream, te tomará más tiempo alcanzar competencia básica con vim. Pero una vez que lo logres, la recompensa también es mayor.

Ahora, Neovim es básicamente infinitamente configurable. Si realmente quieres irte alocado, puedes crear tu propia configuración de Neovim desde cero. Hay un gran curso de [Typecraft sobre configurar Neovim desde cero](https://www.youtube.com/watch?v=zHTeCSVAFNY). Y [ThePrimegean también tiene uno](https://www.youtube.com/watch?v=w7i4amO_zaE).

Pero Omarchy viene con una configuración completa de Neovim que ha sido cuidadosamente ajustada para mostrar lo mejor de lo que es posible hacer desde el primer momento. ¡Sin tener que escribir ni una sola línea de configuración! Se llama [LazyVim](https://www.lazyvim.org/), y es una distribución de plugins y configuraciones de Neovim. Es genial.

## Fundamentos de LazyVim

Como mencioné, no voy a enseñarte vim en esta corta introducción, pero puedo mostrarte algunos fundamentos de LazyVim y cómo moverte.

Primero, Neovim tiene la idea de la tecla líder. Esa es básicamente la puerta de entrada a todos los comandos. LazyVim la ha configurado en `Space`. Así que solo presiona eso, espera un segundo, y verás un montón de opciones explicadas en línea.

Aquí hay algunos comandos básicos que uso todo el tiempo:

- `Space Space` - Buscar cualquier archivo en el directorio actual de forma difusa.
- `Space S G` - Buscar en todos los archivos usando grep con previsualización.
- `Space E` - Alternar el árbol de archivos activado/desactivado.
- `Ctrl + W W` - Saltar del árbol de archivos al editor y viceversa.
- `Shift + H` - Mover a la pestaña de archivo izquierda.
- `Shift + L` - Mover a la pestaña de archivo derecha.
- `Space B D` - Cerrar una pestaña.
- `Space B O` - Cerrar todas las demás pestañas excepto la actual.
- `Space G G` - Lanzar LazyGit en un panel flotante desde el directorio actual.
- `Space U W` - Alternar ajuste suave de línea.

Mientras estás en el árbol de archivos (`Space E` para revelar, `Ctrl + W W` para saltar ahí), puedes agregar un nuevo archivo con `a` o un nuevo directorio con `A`. Presiona `?` mientras estás en el árbol para ver todos los comandos.

Si quieres aprender el lenguaje básico de vim, he escrito sobre [la sintaxis de tres partes](https://world.hey.com/dhh/wonderful-vi-a1d034d3) y cómo ejecutar esos movimientos combinados como un pro.

Puedes ver todos los comandos posibles en [la página de atajos de LazyVim](https://www.lazyvim.org/keymaps).

## Iniciar Neovim

Puedes iniciar Neovim con `Super + Shift + N`, pero generalmente es más fácil manejarlo desde la terminal navegando al directorio en el que quieras trabajar y escribiendo `n`. La `n` es el alias para `nvim`, que usará el directorio presente para abrir por defecto. Puedes abrir un solo archivo con `n miarchivo.txt`.

## Usar Neovim para ediciones con sudo

Si necesitas editar archivos que solo puedes cambiar como superusuario, puedes usar neovim con todos tus plugins configurados ejecutando `sudoedit /etc/sudoers.d/00-solo-archivo-sudo`.
