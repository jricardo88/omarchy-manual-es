# FAQ

## ¿Cómo cambio entre layouts de teclado?

Edita tu archivo `~/.config/hypr/input.conf` y agrega esto para cambiar entre layouts con `Alt Izquierda + Alt Derecha`:

```
# Usar múltiples layouts de teclado y cambiar entre ellos con Alt + Alt
input {
    kb_layout = us,fr
    kb_options = compose:caps,grp:alts_toggle
}
```

Incluso puedes [configurar Waybar para mostrar tu layout de teclado actual en la barra superior](https://github.com/basecamp/omarchy/discussions/111).

---

## ¿Cómo cambio el formato del reloj a 12 horas?

Edita tu archivo `~/.config/waybar/config.jsonc` y reemplaza esto:

```
"clock": {
  "format": "{:%A %H:%M}",
```

con:

```
"clock": {
  "format": "{:%A %I:%M %p}",
```

Esto mostrará Domingo 10:55 AM.

---

## ¿Cómo cambio dónde se guardan las capturas de pantalla o grabaciones?

Si quieres que las capturas se guarden en `~/Pictures/Capturas` en vez de solo `~/Pictures`, puedes abrir *Configurar > Predeterminados* via el menú de Omarchy y configurar esto:

```
export OMARCHY_SCREENSHOT_DIR="$HOME/Pictures/Capturas"
```

Puedes hacer lo mismo para grabaciones de pantalla usando `OMARCHY_SCREENRECORD_DIR`.

Solo recuerda crear el directorio donde quieres guardar y reiniciar Omarchy para que esto surta efecto.

---

## ¿Cómo hago que funcione el altavoz + webcam en mi Apple Studio Display?

Pensarías que debería funcionar todo simplemente conectando USB C, pero lamentablemente ese no es el caso. La solución que he encontrado para que funcione de forma confiable es usar [el cable WJESOG DisplayPort + USB-A => USB-C](https://www.amazon.com/WJESOG-DisplayPort-Adapter-Converter-Thunderbolt/dp/B0BNX7MS6N/). Entonces el altavoz y la webcam funcionan de maravilla.

Recuerda que tienes control de brillo integrado en Omarchy para los Displays Apple (tanto Studio como XDR) usando `Ctrl + F1` para bajar brillo, `Ctrl + F2` para subirlo, y `Ctrl + Shift + F2` para ponerlo al máximo.

---

## ¿Cómo elimino todo el software extra?

Si no quieres programas como Spotify u Obsidian o cualquiera del otro software preinstalado, puedes eliminarlo muy fácilmente.

Ejecuta *Remover > Paquete* para ver cada paquete que está instalado. Luego puedes seleccionar cualquier paquete que quieras eliminar con tab, y empezar a eliminar todo lo que hayas seleccionado con return.

Y puedes usar *Remover > App Web* desde el menú de Omarchy para eliminar cualquiera de las apps web preinstaladas que no quieras.

---

Para errores y problemas rotos, ver [la sección de Solución de problemas](./17-solucion-problemas.md).

---

# Solución de problemas

## ¡Arruiné mi sistema con una actualización!

Primero intenta [revertir tu sistema](./14-actualizaciones.md#instantáneas-del-sistema) a la versión antes de tu actualización reciente. Si eso no funciona, usa `omarchy-debug` para compartir tu problema en \#omarchy-help en Discord. Y si todo falla, puedes reinstalar los configs y paquetes predeterminados usando `omarchy-reinstall`.

---

## ¿Por qué algunas apps son tan grandes en mi pantalla?

Omarchy asume una pantalla de alta resolución 2x, que requiere configurar `GDK_SCALE` a 2 en `~/.config/hypr/hyprland.conf`. Pero si estás en una pantalla 1x, puedes cambiar esto a 1 (y luego reiniciar cualquier app que esté sobredimensionada). Ver [el manual de monitores](./12-monitores.md).

Para Spotify, puedes usar `Ctrl + Menos` para achicar la UI (y `Ctrl + Más` para agrandarla).

---

## ¿Por qué no funciona Caps Lock?

En Omarchy, Caps Lock ha sido designado como la tecla xcompose. Así es como obtienes [emojis rápidos](https://manuals.omamix.org/2/the-omarchy-manual/53/hotkeys#quick-emojis) y [otros autocompletados](https://manuals.omamix.org/2/the-omarchy-manual/53/hotkeys#quick-completions). Si realmente extrañas usar Caps Lock, puedes reasignar la tecla xcompose a algo más editando `~/.config/hypr/input.conf`, como configurándola a la tecla alt derecha:

```
kb_options = compose:ralt
```

---

## ¿Por qué mis parlantes externos no suenan?

Probablemente porque no están configurados como salida principal. Haz clic en el parlante en la parte superior derecha de waybar, y lançará los controles de volumen donde puedes seleccionar el parlante principal (desígnalo como predeterminado con "d").

---

## ¿Por qué no puedo iniciar sesión o hacer sudo con mi contraseña?

Probablemente la escribiste mal demasiadas veces y te bloquearon. Si esto está pasando en la pantalla de bloqueo, puedes presionar `CTRL + ALT + F2` para iniciar una nueva TTY donde puedes hacer login como root, luego ejecutar `faillock --reset --user [tu-usuario]`. Eso restablecerá el bloqueo, y estás listo para seguir.

---

## ¿Por qué no aparecen los avisos de autorización de 1Password para 1Password SSH Agent / CLI?

Esto puede pasar por 2 razones:

Para que aparezca el aviso de aprobación rico, Configuración > Avanzado > Usar Aceleración de Hardware debe estar activado. *Nota: Esto requiere reiniciar para comenzar a funcionar.*

![1Password hw accel](https://jricardo88.github.io/omarchy-manual-images/1pw-hw-accel-w6VzWp.png)

O si no has lanzado 1Password desde que arrancaste, el aviso no aparecerá.
