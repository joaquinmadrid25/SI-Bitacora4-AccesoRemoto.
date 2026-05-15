

# UD07. T01. Elaboración de documentación técnica y uso de aplicaciones de propósito general {#ud07.-t01.-elaboración-de-documentación-técnica-y-uso-de-aplicaciones-de-propósito-general}

Nombre y Apellido: Joaquin Madrid del Toro  
Ciclo: Desarrollo de Aplicaciones Web  
Fecha:15/05/2026

**ÍNDICE**

** Analisis de Necesidades

**1.1. Problema detectado 	…………………………………………………………………………………………..**

**1.2. Solucion propuesta …………………………………………………………………………………………..**

**1.3. Justificacion de la eleccion …………………………………………………………………………………………..**

# Analisis de Necesidades

1.1. Problema detectado:

La empresa necesita una solución que permita gestionar el acceso remoto a diferentes equipos de forma segura, centralizada y sencilla. Actualmente, conectarse directamente mediante RDP a cada máquina genera varios inconvenientes técnicos y de seguridad. Cada ordenador debe configurarse individualmente y exponerse a la red, aumentando el riesgo de accesos no autorizados y complicando la administración de usuarios y permisos.
Además, este sistema provoca una mayor carga de trabajo para el personal técnico, ya que cualquier cambio o incidencia debe resolverse equipo por equipo. También existen problemas de compatibilidad, ya que no todos los usuarios disponen del mismo software cliente para conectarse remotamente. Todo esto reduce la eficiencia y dificulta el mantenimiento de la infraestructura informática.
Por otro lado, la empresa necesita una plataforma que permita acceder a los servicios desde cualquier lugar y dispositivo, manteniendo siempre un entorno controlado y profesional. Por ello, se plantea la necesidad de utilizar una solución centralizada basada en Guacamole y Docker.


1.2. Solucion propuesta:

La solución elegida consiste en implementar Apache Guacamole utilizando contenedores Docker. Guacamole es una herramienta de acceso remoto que funciona desde el navegador web y permite conectarse a diferentes máquinas mediante protocolos como RDP, SSH o VNC sin necesidad de instalar programas adicionales en el equipo del usuario.
Gracias a Docker, la aplicación puede desplegarse de forma rápida, aislada y organizada. La contenedorización facilita el mantenimiento del sistema, evita problemas de dependencias y permite mover la aplicación entre distintos entornos sin modificar la configuración principal. Además, las actualizaciones y copias de seguridad se simplifican considerablemente.
La utilización de una plataforma centralizada permite administrar todas las conexiones desde un único punto, mejorando la organización y reduciendo el tiempo dedicado a tareas de soporte técnico. También se optimizan recursos, ya que no es necesario configurar manualmente cada acceso remoto en todos los equipos de la empresa.

1.3. Justificacion de la eleccion:

Se ha elegido esta solución porque ofrece ventajas importantes frente al acceso directo mediante RDP. La principal mejora es la seguridad, ya que los equipos internos no necesitan estar expuestos directamente a Internet. Todo el acceso se realiza a través de Guacamole, que actúa como intermediario y permite aplicar controles de autenticación y permisos de usuario.
Otra ventaja importante es la centralización. En lugar de gestionar múltiples conexiones individuales, los administradores pueden controlar todos los accesos desde una única interfaz web. Esto facilita enormemente la administración de la infraestructura y permite escalar el sistema de manera más sencilla en el futuro.
Además, el uso de Docker aporta estabilidad y flexibilidad al proyecto. Los contenedores garantizan que la aplicación funcione siempre de la misma manera independientemente del entorno donde se despliegue. Esto reduce errores de configuración y mejora la disponibilidad del servicio.
En conclusión, la implementación de Guacamole sobre Docker permite satisfacer las necesidades de la empresa ofreciendo una solución moderna, segura, escalable y fácil de mantener.

