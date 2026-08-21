# NoxuraSSH

Script de administracion para VPS con menus interactivos orientados a SSH,
protocolos de conexion, usuarios y servicios adicionales.

Desarrollado por: **J DAVID AG**

> Proyecto en desarrollo. Aun se esta mejorando la compatibilidad, el diseno de
> menus y la estabilidad de algunos modulos.

## Sistemas soportados

Sistemas x64 recomendados:

- Ubuntu 18
- Ubuntu 20
- Ubuntu 24
- Debian 9
- Debian 10
- Debian 11
- Debian 12

Notas:

- Para mejor estabilidad use una VPS limpia.
- V2Ray se recomienda principalmente en Ubuntu 18/20 x64.
- Algunas funciones pueden depender del proveedor VPS, firewall, DNS y puertos abiertos.

## Instalacion

Ejecute como root:

```bash
wget -qO noxurassh "https://raw.githubusercontent.com/Davidgelves/NoxuraSSH/main/noxurassh?$(date +%s)" && chmod +x noxurassh && bash noxurassh
```

Despues de instalar, puede abrir el menu con:

```bash
menu
```

## Desinstalacion

Desde el menu principal:

```text
menu
```

Luego seleccione la opcion:

```text
DESINSTALAR SCRIPT
```

Tambien puede ejecutar directamente:

```bash
delscript
```

## Protocolos y servicios disponibles

El script incluye menus para administrar o instalar:

- OpenSSH
- Proxy SOCKS
- SSL Tunnel
- Dropbear
- V2Ray
- SlowDNS
- Hysteria v1
- Trojan-Go
- BadVPN UDPGW
- OpenVPN
- WebSocket Redirector
- SSLH Multiplex
- Squid Proxy
- Chisel
- Panel Web V2Ray
- Apache

## Funciones principales

- Crear, eliminar y administrar usuarios SSH.
- Crear usuarios de prueba.
- Ver usuarios registrados e informe de vencimientos.
- Limitar usuarios por conexiones o consumo.
- Eliminar usuarios vencidos.
- Configurar puertos y servicios.
- Reiniciar servicios desde el menu.
- Administrar V2Ray con UUID, path, TLS y configuracion.
- Administrar SlowDNS con claves, dominio NS, puerto y diagnostico.
- Ver logs de servicios cuando esten disponibles.

## Idioma

El idioma se detecta automaticamente desde `LANG_CHOICE`, `LC_ALL`,
`LC_MESSAGES` o `LANG`.

- `es`, `es_CO`, `es_ES`, etc. usan Espanol.
- `en`, `en_US`, `en_GB`, etc. usan English.
- Cualquier otro idioma usa Espanol como respaldo.

Tambien puede forzarlo:

```bash
sudo LANG_CHOICE=es ./noxurassh
sudo LANG_CHOICE=en ./noxurassh
```

## Estado del proyecto

NoxuraSSH sigue en desarrollo. Se estan ajustando:

- Diseno visual de menus.
- Compatibilidad entre sistemas.
- Instalacion y desinstalacion limpia.
- Modulos V2Ray, SlowDNS, Hysteria y servicios relacionados.

## Aviso

Use este proyecto bajo su propia responsabilidad. Revise el codigo antes de
ejecutarlo en servidores de produccion.
