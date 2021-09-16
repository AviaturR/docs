---
title: Travelport API
slug: /travelport-api-documentation
---

## Introducción
Travelport le permiten crear rápidamente soluciones para buscar y reservar viajes en toda la gama de contenido de proveedores de Travelport para vuelos, hoteles y automóviles.

Este nuevo conjunto de microservicios API modernos se basa en el estándar API de Open Travel Alliance (**OTA**). Utilizan conceptos de metodología de distribución abierta (**ODM**), lo que los hace fáciles de trabajar, estandarizados, confiables y preparados para el futuro.

Todas las API JSON de Travelport ofrecen búsqueda optimizada para dispositivos móviles y un número optimizado de parámetros de solicitud para aumentar el rendimiento y disminuir el tiempo de respuesta. Alguna de sus caraácteristicas más importantes son:

- Respuestas más rápidas y ligeras.
- La oportunidad de construir un Producto Mínimo Viable (**MVP**) en el espacio de búsqueda de viajes.
- Una forma de ponerse al día fácilmente en el dominio de la tecnología de viajes.
- equilibrar la velocidad, el rendimiento y las necesidades de los desarrolladores de búsquedas de viajes.

## Primer Paso
Recibirá un correo electrónico automático invitándolo a completar su registro en _MyTravelport_. Si ya solicitó credenciales de prueba y tiene una cuenta de desarrollador de Sandbox en _MyTravelport_, su cuenta se transferirá a una cuenta de usuario desarrollador o administrador de desarrollador. Acepte los términos y condiciones y actualice la contraseña a una de su elección. Una vez que haya completado su registro:

1. Inicie sesión en https://my.travelport.com
2. Comience con su desarrollo utilizando los enlaces provistos en la opción de **Developer Tools > Travelport JSON API** en el menú.

## Autenticación
Todas las API JSON de Travelport requieren autenticación con _OAuth 2.0._ Antes de llamar a cualquier API, debe seguir un procedimiento de autorización basado en OAuth para obtener un token de acceso y luego proporcionar ese token de acceso con cada llamada.

- Para más información sobre el funcionamiento de _OAuth_ visitar [OAuth 2.0 Authorization Framework](http://https://datatracker.ietf.org/doc/html/rfc6749 "OAuth 2.0 Authorization Framework")

### Access Groups
A todos los usuarios de la API de Travelport JSON se les asignan grupos de acceso. Un grupo de acceso contiene información sobre una organización, incluido el **PCC**, la ubicación, la moneda, la información del operador de **NDC** y **GDS**, los enlaces de impresoras y más. Cada solicitud de autenticación de API requiere un grupo de acceso como parte del envío para generar un token que se puede usar en solicitudes posteriores. El token, creado en parte con el grupo de acceso, garantiza que las respuestas devuelvan datos relevantes para la ubicación específica de una organización.

### Generar Token
Para generar el token de autenticación en el lenguaje de programación de su elección, debe completar las siguientes credenciales proporcionadas cuando se le aprovisionó con las API JSON de Travelport:

- username
- password
- client_id
- client_secret

Envíe su solicitud los siguientes **endpoints**, según corresponda:

- Pre-producción: https://oauth.pp.travelport.com/oauth/oauth20/token
- Producción: https://oauth.travelport.com/oauth/oauth20/token

