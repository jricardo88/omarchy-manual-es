# Primeros pasos

Omarchy se instala usando una imagen ISO. Está diseñado para un disco dedicado, así que el dual-boot requiere dos discos en tu máquina (a menos que hagas una [instalación manual](./18-extras.md#instalación-manual) para evitar esto). La instalación borrará el disco seleccionado y usará encriptación de disco completo, así que ¡haz un backup antes de usar un disco existente!

[Descarga la ISO de Omarchy](https://omarchy.org/) primero, ponla en un USB (usa [balenaEtcher](https://etcher.balena.io/) en Mac/Windows o [caligula](https://github.com/ifd3f/caligula) en Linux), y arranca desde el USB.

*Debes desactivar Secure Boot y/o TPM en la BIOS. Tienes que apagarlos para poder instalar Omarchy. Son esquemas de seguridad de Microsoft pensados para Windows y distribuciones Linux affiliadas a Microsoft.*

Luego responde las preguntas de configuración y confírmalas así:

![Pantalla de confirmación de instalación](https://jricardo88.github.io/omarchy-manual-es/img/omarchy-install-k5Iksv.png)

Después selecciona un disco para tu instalación y sientate a ver el show de la instalación. Toma entre 2 y 10 minutos, dependiendo de la velocidad de tu computadora.

![Instalación completada](https://jricardo88.github.io/omarchy-manual-es/img/omarchy-installed-NR1wu1.png)

¡Ahora estás listo para Omarchy!

---

## ¡Usa un teclado cableado o de 2.4ghz!

La encriptación de disco completo no te permitirá ingresar la contraseña desde un teclado Bluetooth al iniciar. Así como no puedes usar un teclado Bluetooth para entrar a la BIOS en una PC. Necesitarás un teclado que use un dongle de 2.4ghz o un cable (¡que de todas formas es mucho mejor para la latencia!). Personalmente amo el [Lofree Flow84](https://www.lofree.co/products/lofree-flow-the-smoothest-mechanical-keyboard).

---

## Ayuda si te atascas

Si te atascas, generalmente puedes encontrar a alguien dispuesto a ayudar en el canal *\#omarchy-help* en el [Discord de la comunidad](https://omarchy.org/discord).

---

## Usa instalación manual para necesidades especiales

Si tienes necesidades especiales, como instalar Omarchy en MacBooks con chips M-series [Asahi Alarm](https://asahi-alarm.org/) o porque quieres probar dual-boot en un solo disco, deberías seguir [las instrucciones de instalación manual](./18-extras.md#instalación-manual).

---

← [Anterior: Bienvenida](01-bienvenida.md) | [Índice](../README.md) | [Siguiente: Navegación →](03-navegacion.md)
