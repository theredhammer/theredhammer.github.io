---
title: 1.2 Cryptography and VPNs
author: redhammer
date: 2022-12-01 11:33:00 +0800
categories: [eJPT, Curso]
tags: [guia_de_estudio, eJPT]
render_with_liquid: false
pin: false
math: true
mermaid: true
---

¿Cómo ayuda esto a mi carrera como pentester?

- Entendiendo como la información es trasmitida a través de las redes informáticas
- Eligiendo el protocolo correcto para la actividad
- Conociendo como proteger nuestro trafico.

¿Por qué introducimos la criptografía aquí?

El objetivo principal de este capitulo es introducir conceptos que nos serán útiles a través del curso.

Ahora explicaremos la diferencias entre texto claro y protocolos criptograficos.

Adicionalmente aprenderemos que es una VPN (Virtual Private Network) y como funciona. Todos nuestros laboratorios virtuales usan VPN así que conocer que es nos ayudara a obtener mas de este curso.

## 1.2.1 Cleart-text Protocols

Los protocolos de texto claro transmiten datos a través de la red sin ningún tipo de transformación o encriptación.

Esto deja a un atacante escuchar a escondida la comunicación, así como realizar otras acciones malintencionadas.


![Desktop View](/assets/img/eJPT/1.Introduction/1.2 Cryptography and VPNs/Pasted image 20221130191222.png){: width="972" height="589" }

Debido a su naturaleza, los protocolos de texto claro son fáciles de interceptar, escuchar a escondidas y mutilar. Deberían no ser usados para transmitir información critica o privada.

Si no hay ninguna otra alternativa al protocolo de texto claro, la puedes usar pero solo en redes conocidas.

## 1.2.2 Cryptographic Protocols

Por la otra parte tenemos los protocolos criptográficos, encriptación. Estos transforman la información transmitida para proteger la comunicación.

Los protocolos de criptografía tiene muchas metas distintas. Una es para evitar escuchas.

Si un atacante intercepta el trafico, no serán capaces de entenderlo. 

![Desktop View](/assets/img/eJPT/1.Introduction/1.2 Cryptography and VPNs/Pasted image 20221130191726.png){: width="972" height="589" }

Si necesitas transmitir información privada, por ejemplo un usuario y contraseña, deberías siempre usar el protocolo criptográfico para proteger la comunicación sobre la red.

¿Y si necesitas ejecutar un protocolo de texto claro en una red desconocida?

Puedes enrollar (tunnel) un protocolo de texto claro en uno criptográfico.


![Desktop View](/assets/img/eJPT/1.Introduction/1.2 Cryptography and VPNs/Pasted image 20221130191943.png){: width="972" height="589" }

Un gran ejemplo de tunneling es una VPN

### 1.2.3 Virtual Private Network

Una Red Privada Virtual (VPN)  usa la criptografía para extender una red privada sobre una publica como puede ser internet.

La extensión se hace realizando una conexión protegida a una red privada (como la red de tu oficina o tu red domestica).

![Desktop View](/assets/img/eJPT/1.Introduction/1.2 Cryptography and VPNs/Pasted image 20221130192213.png){: width="972" height="589" }

Desde el punto de vista del cliente, estar en una VPN es lo mismo que estar conectado a una red privada.

Por ejemplo, cuando lances el Laboratorio Hera desde tu área de miembros, un túnel VPN es creado, dejándote a ti conectarte directamente a la red del Laboratorio.

Cuando estas conectado vía VPN, realmente estar corriendo los mismos protocolos que la red privada.

Esto te deja realizar incluso operaciones de red de bajo nivel. Por ejemplo en caso de que uses un packet sniffer como Wireshark.

