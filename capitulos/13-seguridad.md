# Seguridad

Omarchy se toma la seguridad extremadamente en serio. Este está pensado para ser un sistema operativo que puedas usar para hacer *Trabajo Real* en el *Mundo Real*. Donde perder una laptop no pueda llevar a una emergencia de seguridad. Así que esto es lo que hacemos:

1. *Encriptación de disco completo es obligatoria*: Este es el paso más importante para asegurar la protección física de tus datos. Si tu computadora se pierde o es robada, los datos están completamente encriptados usando LUKS estándar (Linux Unified Key Setup).

2. *Firewall habilitado por defecto*: Todo el tráfico entrante está bloqueado por defecto excepto el puerto 22 para ssh y el puerto 53317 para [LocalSend](https://localsend.org/). Incluso bloqueamos el acceso a Docker usando la configuración de [ufw-docker](https://github.com/chaifeng/ufw-docker) para evitar que tus contenedores queden accidentalmente expuestos al mundo.

3. *Arch siempre tiene las últimas actualizaciones*: Arch, la distribución subyacente en la que está construido Omarchy, es una distribución rolling. Esto significa que cualquier vulnerabilidad de seguridad que se descubra y parche en cualquier paquete está inmediatamente disponible para instalar usando `yay -Syu`. Siempre estás ejecutando las versiones más recientes y seguras de todo de esta manera.

4. *Omarchy mantiene sus propios paquetes y espejo*: Omarchy solo depende de paquetes de los repositorios core/extra/multilib de Arch y su propio Repositorio de Paquetes de Omarchy por defecto. Puedes instalar software directamente desde AUR, pero Omarchy no lo hace por defecto. Ni siquiera para las instalaciones opcionales.

5. *Cloudflare nos protege de DDoS*: Toda la infraestructura de distribución de Omarchy — las ISOs, los paquetes de Omarchy, el espejo de Arch — está protegida tras el formidable escudo DDoS de Cloudflare y hospedada en su CDN. Esto proporciona una disponibilidad soberbia.

## Claves de firma

La clave pública para todas las firmas de ISO y paquetes del repositorio de Omarchy es `40DFB630FF42BCFFB047046CF0134EE680CAC571` ([verifica en openpgp.org](https://keys.openpgp.org/search?q=pkgs%40omarchy.org)). El paquete `omarchy/omarchy-keyring` también contiene esto y se usará para desplegar cualquier actualización potencial sin problemas.

Puedes encontrar la firma para cualquier lanzamiento de ISO agregando .sig a la URL. Como <https://iso.omarchy.org/omarchy-x.x.x.iso.sig>.

---

# Autenticación biométrica

## Huella digital

Muchas laptops, como mi amada [Framework 13](https://frame.work/laptop13), vienen con un sensor de huella digital para hacer autenticación. Puedes usar esto con Omarchy ejecutando *Configurar > Seguridad > Huella Digital* en el menú de Omarchy (`Super + Alt + Space`). Eso instalará el paquete de huella digital,收集 tu huella, la verificará, y estarás listo para ir usando tu huella para desbloquear desde la pantalla de bloqueo (que puedes activar con `Super + Escape`), entrar en modo sudo y autorizar avisos del sistema.

Si has configurado autenticación de huella digital, pero luego necesitas trabajar en un teclado externo que no la tiene, solo presiona `CTRL + C` cuando se te pida tu huella durante `sudo`.

Puedes remover la autenticación de huella digital bajo *Remover > Huella Digital* en el menú de Omarchy.

Tanto agregar como remover autenticación de huella digital también está disponible a través de la TUI de Omarchy bajo el menú Configurar.

## Autenticación Fido2

Si estás usando un dispositivo Fido2, puedes configurarlo para autenticación `sudo` usando *Configurar > Seguridad > Fido2* en el menú de Omarchy (`Super + Alt + Space`). Solo es para `sudo`, aunque, no para desbloquear tu computadora.

Puedes remover la autenticación fido2 bajo *Remover > Fido2* en el menú de Omarchy.
