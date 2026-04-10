# Monitores

Omarchy asume que estás ejecutando en una pantalla retina de clase 2x por defecto. Esto es lo que necesitas para esas fuentes de programador nítidas y hermosas. Es lo que laptops como la Framework 13 con su monitor 2.8K está optimizado. Es lo que querrías ejecutar en un Apple Studio Display de 27" 5K, ProArt PA27JCV, Samsung S9 o Kuycon G27P de 27", o Apple XDR de 32" 6K, ProArt PA32QCV o Kuycon G32P.

Así que si no estás ejecutando una pantalla con PPI de 218 o superior, vas a querer cambiar la configuración del monitor. Por ejemplo, si tienes un monitor de 27" o 32" 4K, puedes usar escalado fraccionario abriendo `~/.config/hypr/monitors.conf` y cambiando a la recomendación para esa combinación:

```
env = GDK_SCALE,1.75
monitor=,preferred,auto,1.666667
```

Si estás usando una pantalla 1080p o 1440p, probablemente solo quieras usar escalado 1x, así que puedes usar:

```
env = GDK_SCALE,1
monitor=,preferred,auto,1
```

Los cambios a `GDK_SCALE` aplican a aplicaciones iniciadas después del cambio. Así que asegúrate de cerrar las ventanas que tengas sobredimensionadas después del cambio (¡o cierra todas las ventanas con `Ctrl + Alt + Del`!).

También puedes ciclar rápidamente entre las proporciones de escala de monitor principales (1x, 1.6x, 2x, 3x) usando `Super + /`.

Solo ten en cuenta que es ejecutar Linux en pantallas de baja resolución y usar escalado fraccionario lo que le ha dado a la plataforma una mala reputación por fuentes quisquillosas. Es una situación completamente autoinfligida. ¡Con una pantalla de clase retina (218ppi+) y escalado 2x, tus fuentes se verán tan geniales en Linux como lo harían en Mac (¡si no mejor, porque no se aplica suavizado de fuentes artificial por encima de lo que el diseñador de fuentes pretendía!)!

---

## Organizando múltiples pantallas

Hyprland funciona genial con múltiples pantallas. Lee más sobre cómo disponerlas en [la documentación de monitores de Hyprland](https://wiki.hypr.land/Configuring/Monitors/). También puedes [vincular workspaces específicos a monitores específicos](https://wiki.hypr.land/Configuring/Workspace-Rules/).

También puedes revisar [Hyprmon](https://github.com/erans/hyprmon/), si quieres una TUI para ayudarte con el posicionamiento de múltiples pantallas.
