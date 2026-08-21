# NoxuraSSH (version saneada)

Este proyecto fue ajustado para uso mas seguro de BadVPN UDPGW en Debian/Ubuntu.

## Cambios de seguridad

- Se elimino el flujo de instalacion por `bash <(wget ...)`.
- El entrypoint `noxurassh` ya no descarga ni ejecuta scripts remotos.
- Se usa instalador local: `instalar-badvpn-seguro.sh`.
- Se configura `systemd` en lugar de `screen` + `/etc/autostart`.
- No se usa `chmod 777`.

## Instalacion recomendada

Copiar la carpeta al VPS y ejecutar:

```bash
chmod +x ./noxurassh ./instalar-badvpn-seguro.sh
sudo ./noxurassh
```

## Idioma / Language

El idioma se detecta automaticamente desde `LANG_CHOICE`, `LC_ALL`,
`LC_MESSAGES` o `LANG`:

- `en`, `en_US`, `en_GB`, etc. usan English.
- `es`, `es_CO`, `es_ES`, etc. usan Espanol.
- Cualquier otro idioma usa Espanol como respaldo.

Si ejecutas el instalador en una terminal interactiva y no usas `LANG_CHOICE`,
se pedira el idioma al inicio y se guardara en `/etc/SSHPlus/lang` para el menu.

Tambien puedes forzarlo por variable:

```bash
sudo LANG_CHOICE=es ./noxurassh
sudo LANG_CHOICE=en ./noxurassh
```

## Variables opcionales

```bash
sudo PORT=7301 MAX_CLIENTS=2000 ./instalar-badvpn-seguro.sh
```

## Verificacion

```bash
systemctl status badvpn-udpgw
journalctl -u badvpn-udpgw -f
ss -lntp | grep 7300
```
