# Actualizaciones

Omarchy y tus paquetes se mantienen actualizados via *Actualizar > Omarchy* en el menú de Omarchy (`Super + Alt + Space`).

Esto obtiene [el último código y configuraciones de Omarchy](https://github.com/basecamp/omarchy/releases), ejecuta cualquier migración pendiente para poner tu sistema en sync con lo último, y actualiza todos los paquetes del sistema desde el [Espejo Arch de Omarchy](https://github.com/omacom-io/omarchy-mirror), [Repositorio de Paquetes de Omarchy](https://github.com/omacom-io/omarchy-pkgs) y [AUR](https://aur.archlinux.org/) (si has instalado algún paquete de AUR).

Cuando hay nuevos lanzamientos, aparecerá un icono de flecha circular a la derecha de tu reloj. Haz clic en él y el proceso de actualización comenzará.

![Indicador de actualización](https://jricardo88.github.io/omarchy-manual-images/screenshot-2025-09-28_19-06-08-yZI06N.png)

---

## Cuatro canales

Omarchy se actualiza a lo largo de cuatro canales: stable, RC, edge y dev. Las nuevas instalaciones comienzan en el canal stable, que sigue los [lanzamientos oficiales](https://github.com/basecamp/omarchy/releases/), así como el [espejo Arch estable de Omarchy](https://github.com/omacom-io/omarchy-mirror) que va un mes detrás de lo último, así podemos detectar cualquier incompatibilidad nueva que requiera cambios de configuración antes de que cause problemas a la gente.

Pero si te gustaría ayudar a detectar esos problemas potenciales, puedes ejecutar en el canal edge. Eso mantendrá el código de Omarchy siguiendo los lanzamientos oficiales, pero te permite actualizar a los paquetes de Arch más recientes tan pronto como estén disponibles. Solo deberías hacer esto si tienes experiencia con Linux y sabes cómo recuperar un sistema que tiene problemas.

Antes de cualquier nuevo lanzamiento mayor, estaremos haciendo validación final usando el canal RC. Si estás interesado en ayudar con el pulido final, ven al canal \#omarchy-release-candidates en el Discord.

Finalmente, está el canal dev, que te da los cambios de código más recientes de Omarchy y los paquetes edge. Solo deberías usar este canal si eres un usuario de Linux experimentado, trabajando directamente en Omarchy, y dispuesto a tolerar interrupciones.

Puedes cambiar entre canales usando *Actualizar > Canal* desde el menú de Omarchy.

---

## Advertencia sobre actualizaciones directas de pacman/yay

Si ya estás familiarizado con Arch, podrías estar tentado a solo ejecutar `pacman -Syu` o `yay -Syu` tú mismo, pero si haces eso, corres el riesgo de perder actualizaciones de los archivos de configuración necesarios para soportar versiones más nuevas de librerías o herramientas. Así que es mejor quedarse con `Actualizar > Omarchy`, así estás seguro de que cualquier migración se ejecuta junto con los paquetes nuevos.

---

## Revertir actualizaciones malas

Si alguna vez tienes un problema después de hacer una actualización, puedes revertir tu sistema a la instantánea tomada antes de la actualización. Solo reinicia y pick the snapshot en el menú de carga de arranque desde antes de que iniciaras la actualización.

![Bootloader de Omarchy](https://jricardo88.github.io/omarchy-manual-images/omarchy-bootloader-EVTCUU.png)

Si de alguna manera tus archivos de configuración han sido corrompidos, también puedes realizar una reinstall de Omarchy usando `omarchy-reinstall` en la terminal. Esto restaurará tu instalación de Omarchy al último lanzamiento, te pondrá en stable y degradará cualquier paquete, y restablecerá todos los archivos de configuración. Nota que todos tus cambios de configuración de usuario a los predeterminados de Omarchy serán sobrescritos haciendo esto.

---

# Instantáneas del sistema

Creamos instantáneas automáticamente en cada actualización de Omarchy, pero si quieres crear las tuyas, puedes usar `omarchy-snapshot create`.

Para bootear y restaurar una instantánea, la seleccionas desde el cargador de arranque Limine. (Si actualmente estás arrancando directamente a la pantalla de desencriptación de Omarchy, necesitarás seleccionar Limine como opción de arranque via la BIOS primero).

Desde esa pantalla, elige la instantánea que te gustaría bootear basada en la fecha y versión. La versión de Omarchy en el momento de la instantánea se puede ver en la esquina inferior izquierda.

![Bootloader de Omarchy](https://jricardo88.github.io/omarchy-manual-images/omarchy-bootloader-Qz7kQ1.png)

Cuando llegues adentro, aparecerá un aviso notificándote que estás en una instantánea booteable y si haces clic en él, comenzará el proceso de restauración. Alternativamente, puedes utilizar `omarchy-snapshot restore`.

![Restaurar instantánea](https://jricardo88.github.io/omarchy-manual-images/omarchy-restore-snapshot-2TrMhj.png)

Esto restaurará tu `/root`, pero no tu `/home`. Así que funciona para revertir una actualización de sistema rota, pero no para recuperar archivos personales perdidos.

Esto también significa que tu directorio `~/.config` se mantiene como está. Así que si estás revirtiendo a una versión anterior de una librería o aplicación que almacena archivos de configuración en un formato nuevo, tendrás que resolver eso manualmente.

*Nota: Esta característica solo está disponible en instalaciones usando el cargador de arranque Limine, que ha sido el predeterminado desde Omarchy 2.0. No está disponible si estás en GRUB o systemd-boot.*
