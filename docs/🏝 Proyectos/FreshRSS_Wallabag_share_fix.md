---
title: FreshRSS & Wallabag arreglo para botón "compartir"
tags: sobre/dev sobre/docker sobre/selfhosted sobre/soluciones
---


# General

| Fecha |  Wallabag |  FreshRSS | 
|:--:|:--:|:--:|
| 12-04-2022 | 2.4.3[^Wallabag] | 1.19.2[^FreshRSS]  | 

[^Wallabag]: Contenedor Docker (`lscr.io/linuxserver/freshrss`) corriendo en una RPi4 con  Raspberry Pi OS  <small>(64-bit, Debian 11 Bullseye)</small>

[^FreshRSS]: Contenedor Docker (`ikaruswill/wallabag:2.4.3`) corriendo en una RPi4 con Raspberry Pi OS <small>(64-bit, Debian 11 Bullseye)</small>


# Descripción

Integración FreshRSS & Wallabag (botón compartir):

![](Imags/FreshRSS_Wallabag_compartir_arreglo/boton_compartir.png)

Al pinchar el botón de _"Compartir"_ y seleccionar la opción _"Wallabag"_, si la integración es la correcta, la noticia mostrada en **FreshRSS** se archiva automáticamente en **Wallabag** sin más interacción


# Problema 

- Configuración por defecto que no funciona:   `wallabag://wallabag@http://192.168.1.232:8084/`

	![[no_funciona.png]]

- Genera la URL:
	
	```js
	wallabag://wallabag@http://192.168.1.232:8084//bookmarklet?url=https%3A%2F%2Fwww.microsiervos.com%2Farchivo%2Fenergia%2Fexplorador-datos-energia-electricidad-2022.html
	```

![[problema.png]]


# Añadir URL desde navegador

- Añadir desde el navegador funciona con:

	```js
	http://192.168.1.232:8084/bookmarklet?url=
	```

>- Fuente: [ GItHub Wallabag | Issue 2130 ](https://github.com/wallabag/wallabag/issues/2130)
>
>```js
javascript:var url=location.href||url;var wllbg=window.location.replace('https://url.com/web/bookmarklet?url=' + encodeURI(url));void(0);
>```

# Solución 

- Configuración que funciona:  `http://192.168.1.232:8084` 
  -  ⚠ **IMPORTANTE**: debe ir sin la barra `/` al final

	![[si_funciona.png]]

- Genera la URL correcta:

```js
http://192.168.1.232:8084/bookmarklet?url=https%3A%2F%2Fwww.onmsft.com%2Fnews%2Fsurface-laptop-go-2-reportedly-coming-soon
```
