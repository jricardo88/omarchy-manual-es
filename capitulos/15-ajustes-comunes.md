# Ajustes comunes

Esta es una colección de personalizaciones comunes a la configuración de Omarchy. Ten en cuenta que ocasionalmente puede ser necesario que las actualizaciones del sistema restauren ciertos configs a su condición original. Si esto pasa, tus cambios no se perderán, pero se pondrán en un archivo `.bak` en el mismo directorio.

Si arruinas algo, puedes restaurar configs individuales a su configuración original via *Actualizar > Config* en el menú de Omarchy. Si *realmente* arruinas todo, puedes restablecer todos los configs via `omarchy-reinstall`.

---

## Revelar todos los iconos de bandeja todo el tiempo

Por defecto, los iconos de bandeja, como Dropbox, 1password o Steam, están escondidos detrás del icono expansor de bandeja. Si quieres tenerlos expuestos todo el tiempo, puedes cambiar la línea `group/tray-expander` a `tray` en el `config.jsonc` de Waybar (`~/.config/waybar/config.jsonc`, acceso via *Configurar > Config > Waybar*).

---

## Esquinas de ventana redondeadas

El diseño por defecto de Omarchy tiene esquinas cuadradas, pero si te gusta suavizar eso un poco, puedes cambiar `~/.config/hypr/looknfeel.conf` para que el redondeo ya no esté comentado:

```
decoration {
    # Usar esquinas de ventana redondeadas
    rounding = 8
}
```

---

## Eliminar espacios entre ventanas

En pantallas de laptops, algunas personas prefieren no desperdiciar ningún píxel en espacios entre ventanas (o incluso una barra superior, que puedes alternar con `Super + Shift + Space`). Puedes eliminar todos los espacios removiendo los comentarios en esta sección de `~/.config/hypr/looknfeel.conf`:

```
general {
    # Sin espacios entre ventanas o bordes
    gaps_in = 0
    gaps_out = 0
    border_size = 0
}
```

---

## Portapapeles unificado

Por lo general en Linux necesitas `Ctrl + Shift + C/V` para copiar y pegar en la terminal y `Ctrl + C/V` para hacerlo en todos lados. Eso es difícil de习惯了 para cualquiera que no haya nacido y crecido en Linux. También lo es el cambio de super a ctrl, si vienes del Mac.

Omarchy aborda ambos problemas con atajos de portapapeles unificados que funcionan (casi) en todas partes:

| Atajo | Comando |
|-------|---------|
| `Super + C` | Copiar |
| `Super + X` | Cortar |
| `Super + V` | Pegar |
| `Super + Ctrl + V` | Historial del portapapeles |

*Las dos excepciones a esta uniformidad son el administrador de archivos (Nautilus) y las CLIs de Agentes AI (OpenCode, Claude Code). Ahí infelizmente tendrás que conformarte con `Ctrl + C/X/V` para operaciones de portapapeles.*

### Historial del portapapeles

El historial del portapapeles es proporcionado por Walker y funciona tanto para texto como imágenes. Lo activas con `Super + Ctrl + V`, seleccionas tu entrada con return, y eso se colocará en el portapapeles listo para pegar con `Super + V`.

![Historial del portapapeles](https://jricardo88.github.io/omarchy-manual-es/img/clipbord-history-soxtYp.png)

También puedes buscar en el historial simplemente empezando a escribir:

![Búsqueda en historial](https://jricardo88.github.io/omarchy-manual-es/img/clipboard-history-search-S0PjCI.png)

---

← [Anterior: Actualizaciones](14-actualizaciones.md) | [Índice](../README.md) | [Siguiente: FAQ y Solución de problemas →](16-faq-solucion.md)
