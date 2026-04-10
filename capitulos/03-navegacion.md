# Navegación

En Omarchy todo funciona mediante el teclado — ¡TODO! Cuando el sistema inicia por primera vez, literalmente no puedes hacer nada solo con el mouse. Pero puedes presionar `Super + Space` para abrir el lanzador de aplicaciones y `Super + Alt + Space` para abrir el Menú de Omarchy. Estos dos comandos te permiten hacer prácticamente todo.

Pero el lanzador de aplicaciones no está pensado para ser la forma principal de operar el sistema la mayor parte del tiempo. Podemos ir más rápido que eso. Las aplicaciones más importantes están vinculadas directamente a atajos de teclado individuales. Inicias la terminal con `Super + Return` y un navegador con `Super + Shift + Return`. Prueba hacer uno después del otro y verás la magia del tiling de Hyprland en acción:

![Navegación con navegador y terminal](https://jricardo88.github.io/omarchy-manual-es/img/browser-terminal-yCV75f.png)

Puedes presionar `Super + J` para apilarlos horizontalmente en vez de verticalmente:

![Ventanas apiladas](https://jricardo88.github.io/omarchy-manual-es/img/stacked-sswEJE.png)

Presiona `Super + J` de nuevo para volver a las posiciones horizontales. Luego prueba `Super + Shift + Flecha Derecha` mientras estás en el navegador para intercambiar las ventanas.

Ahora prueba `Super + Ctrl + T` para iniciar el monitor de actividad. Aparecerá como una ventana flotante. Puedes ponerla en tiling usando `Super + T` (y presiona de nuevo para volver a hacerla flotante). Ahora presiona `Super + Shift + F` para abrir el administrador de archivos. Tendrás una configuración genial de cuatro vías:

![Tiling de cuatro ventanas](https://jricardo88.github.io/omarchy-manual-es/img/fourway-tiling-SHbfzO.png)

Navegas entre la ventana que quieras tener activa con `Super + Flecha`. Esto cambiará el foco y moverá el cursor al centro de la nueva aplicación.

Si presionas `Super + Shift + 2`, moverás la aplicación actualmente enfocada al segundo workspace. `Super + Shift + 1` la mueve de vuelta. (Y `Super + Shift + Alt + 2` moverá la aplicación enfocada al segundo workspace sin cambiar a él).

Si mantienes presionado `Super` y usas el mouse para hacer clic en una ventana, podrás reorganizar dónde se coloca. Si mantienes `Super` y usas el botón derecho del mouse, puedes redimensionar libremente la ventana.

Cierras una ventana con `Super + W` (y cierras todas las ventanas con `Ctrl + Alt + Delete`).

También puedes pasar a pantalla completa con `Super + F` o solo ancho completo (manteniendo la barra superior) con `Super + Alt + F`.

---

## Layout dwindle vs scrolling

El layout por defecto de Omarchy se llama dwindle. Mantiene todas las ventanas que abres en un solo workspace visibles todo el tiempo, aunque tenga que achicarlas.

![Layout dwindle](https://jricardo88.github.io/omarchy-manual-es/img/dwindle-layout-BNU9qb.png)

Pero también puedes elegir convertir un workspace en el layout scrolling donde las ventanas se alinean lado a lado, más allá del borde visible de la pantalla. Convietes un solo workspace en este layout via `Super + L`.

![Layout scrolling](https://jricardo88.github.io/omarchy-manual-es/img/niri-layout-LvV25i.png)

Si quieres usar el layout scrolling como predeterminado, puedes configurarlo en `~/.config/hypr/looknfeel.conf` bajo `general { layout = scrolling }`.

---

## Agrupando ventanas

Las ventanas pueden agruparse usando `Super + G`. Una vez que estás en un grupo, cada ventana que inicies mientras esté activo pertenecerá al grupo. Puedes moverte entre estas ventanas agrupadas usando `Super + Ctrl + Flechas` o `Super + Alt + 1/2/3/4` para ir directamente a la ventana agrupada en orden.

Puedes sacar una ventana del grupo con `Super + Alt + G` o desarmar todo el grupo presionando `Super + G` de nuevo. Finalmente, puedes mover ventanas fuera del grupo hacia él con `Super + Alt + Flechas`.

---

## Workspace scratchpad

Finalmente, hay un workspace especial de scratchpad que se superpone sobre el workspace en el que estés actualmente. Accedes a lo que hay ahí usando `Super + S` y colocas ventanas ahí usando `Super + Alt + S`.

Funciona bien para controles o quizás una terminal que quieras usar rápidamente en una superposición sin dejar el workspace actual. Si quieres mover una ventana fuera del scratchpad, simplemente muévela directamente a otro workspace con algo como `Super + Shift + 1` para moverla al workspace 1.

---

## ¡Lleva un poco acostumbrarse!

Lleva un tiempo acostumbrarse a navegar tu escritorio así, pero una vez que lo haces, ¡es difícil volver a la experiencia tradicional de escritorio basada en mouse!

---

← [Anterior: Primeros pasos](02-primeros-pasos.md) | [Índice](../README.md) | [Siguiente: Atajos de teclado →](04-atajos.md)
