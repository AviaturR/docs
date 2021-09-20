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

### Generar Token Postman
Los siguientes pasos detallan cómo ingresar sus credenciales y generar el token OAuth de la colección Travelport Postman Developer Toolkit en la página de [Descargas](https://support.travelport.com/webhelp/TripServices/Content/Downloads/Downloads.htm "Descargas").

#### Ingresar Credemciales

1. Abra la colección Postman y haga clic en la pestaña **Body** en la parte superior de la colección. Complete las siguientes credenciales:
    - username
    - password
    - client_id
    - client_secret

![](https://support.travelport.com/webhelp/TripServices/Content/Resources/Images/oauth/pm_credentials.jpg)

2. A continuación, abra el archivo de entorno: En la esquina superior derecha de la ventana de Postman, seleccione el archivo de entorno que corresponda a su colección y haga clic en el botón de vista rápida del entorno.

![](https://support.travelport.com/webhelp/TripServices/Content/Resources/Images/oauth/pm_editenv.jpg)

3. En la sección **Globals**, coloque el cursor sobre el campo **Access Group** como se muestra a continuación y haga clic en el ícono de lápiz para abrir los campos y editarlos.

![](https://support.travelport.com/webhelp/TripServices/Content/Resources/Images/oauth/pm_accessgroup.jpg)

4. Ingrese el valor del grupo de acceso proporcionado en los campos **Initial Value** y **Current Value**.

5. Haga clic en cualquier lugar fuera de la ventana del entorno para cerrarla y guardar sus cambios.

#### Enviar Token
En cualquier colección de Travelport en Postman, siga los siguientes pasos detallados para ingresar sus credenciales y generar el token OAuth.

1. Abra la colección Postman y expanda la carpeta etiquetada para OAuth como se muestra a continuación.

![](https://support.travelport.com/webhelp/TripServices/Content/Resources/Images/oauth/pm_collection.jpg)

2. Seleccione la transacción POST OAuth adecuada, si hay más de una, y haga clic en el botón **Send** para ejecutarla. El token de acceso consta de todo el texto entre las comillas después de **access_token**.

![](https://support.travelport.com/webhelp/TripServices/Content/Resources/Images/oauth/pm_gentoken.jpg)

3. Ahora puede ejecutar cualquier transacción en el kit de herramientas para desarrolladores.

## Air APIS
La colección Travelport JSON Air API es la conexión basada en API para contenido aéreo integral de múltiples fuentes que permite el rápido desarrollo de soluciones de viaje de alto rendimiento. Las API de Air facilitan el desarrollo multicanal en plataformas web y móviles. Al igual que con otras API JSON de Travelport, todas las solicitudes son RESTful y admiten JSON.

Las API de Air han introducido soporte para contenido de nueva capacidad de distribución (NDC) además del contenido GDS estándar. Esta tecnología conecta a los agentes de viajes con el sistema de una aerolínea y brinda acceso a contenido diferenciado que a menudo solo está disponible a través de los canales directos de las aerolíneas. Las API de Travelport JSON han sido certificadas para contenido NDC con Qantas Airlines, United Airlines, American Airlines y Singapore Airlines. Obtenga más información sobre el contenido de [NDC y GDS](https://support.travelport.com/webhelp/TripServices/Content/Air/NDC.htm "NDC y GDS").

### Air Workflow
Las siguientes API de Air están actualmente en producción y respaldan el flujo de trabajo de Air completo desde la compra hasta la emisión de boletos de un PNR:

Search        | Price         | Book         | Ticket
------------- | ------------- | ------------ | ------------
Busca la disponibilidad de los vuelos que necesites  | Confirme el precio de un itinerario específico con  | Reserve el itinerario aéreo | Consiga el Ticket de su reserva 


### Air Endpoints
Los Endpoint y las solicitudes HTTP disponibles para todas las API de Air se enumeran en la siguiente tabla. Cada solicitud HTTP va seguida de una ruta adicional para agregar al Endpoint, si es necesario, y un enlace a los detalles sobre el envío de esa solicitud.

Los Endpoints de preproducción y producción se proporcionan a continuación en el modelo ODM 10v6, a menos que se indique lo contrario. Los Endpoint de producción solo se pueden usar una vez que esté aprovisionado.

### Search One Way
**Post**
> /air/search/catalogofferings?view=detail

**Headers**

KEY                  | VALUE
-------------------- | -------------
Accept               | application/json
Content-Type         | application/json 
Accept-Version       | **{{version}}**
Content-Version      | **{{version}}** 
Authorization        | **{{token}}**
XAUTH_TRAVELPORT_ACCESSGROUP  | **{{XAUTH_TRAVELPORT_ACCESSGROUP_1G}}**

**Request**
```javascript
{
   "CatalogOfferingsQueryRequest": {
      "CatalogOfferingsRequest": [
         {
            "@type": "CatalogOfferingsRequestAir",
            "contentSourceList": [
               "GDS"
            ],
            "offersPerPage": 100,
            "returnBrandedFaresInd": false,
            "PassengerCriteria": [
               {
                  "number": 1,
                  "age": 25,
                  "passengerTypeCode": "ADT"
               }
            ],
            "SearchCriteriaFlight": [
               {
                  "@type": "SearchCriteriaFlight",
                  "departureDate": "{{InitialDeparture}}",
                  "From": {
                     "value": "LGA"
                  },
                  "To": {
                     "value": "ORD"
                  }
               }
            ],
            "SearchModifiersAir": {
               "excludeGround": "Train"
            }
         }
      ]
   }
}
```

**Response**
```javascript
{
    "CatalogOfferingsResponse": {
        "CatalogOfferings": {
            "@type": "CatalogOfferings",
            "Identifier": {
                "value": "16d41878-4912-442c-83c9-7c240a92f581"
            },
            "DefaultCurrency": {
                "code": "AUD"
            },
            "CatalogOffering": [
                {
                    "@type": "CatalogOffering",
                    "id": "o0.0",
                    "ProductOptions": [...],
                    "Price": {...},
                    "TermsAndConditions": {...}
                },
                ...
            ]
        },
        "ReferenceList": [
            ...
        ]
    }
}
```

### Search Round Trip
**Post**
> /air/search/catalogofferings?view=detail

**Headers**

KEY                  | VALUE
-------------------- | -------------
Accept               | application/json
Content-Type         | application/json 
Accept-Version       | **{{version}}**
Content-Version      | **{{version}}** 
Authorization        | **{{token}}**
XAUTH_TRAVELPORT_ACCESSGROUP  | **{{XAUTH_TRAVELPORT_ACCESSGROUP_1G}}**

**Request**
```javascript
{
  "CatalogOfferingsQueryRequest" : {
    "CatalogOfferingsRequest" : [ {
      "@type" : "CatalogOfferingsRequestAir",
      "maxNumberOfOffersToReturn" : 9999,
      "offersPerPage" : 200,
      "returnBrandedFaresInd" : true,
      "PassengerCriteria" : [ {
        "number" : 1,
        "passengerTypeCode" : "ADT"
      } ],
      "SearchCriteriaFlight" : [ {
        "departureDate" : "{{GDSInitialDepartureDt}}",
        "From" : {
          "value" : "CCU"
        },
        "To" : {
          "value" : "PNQ"
        }
      }, {
        "departureDate" : "{{SixDaysTrip}}",
        "From" : {
          "value" : "PNQ"
        },
        "To" : {
          "value" : "CCU"
        }
      } ]
    } ]
  }
}
```

**Response**
```javascript
{
    "CatalogOfferingsResponse": {
        "CatalogOfferings": {
            "@type": "CatalogOfferings",
            "Identifier": {
                "value": "16d41878-4912-442c-83c9-7c240a92f581"
            },
            "DefaultCurrency": {
                "code": "AUD"
            },
            "CatalogOffering": [
                {
                    "@type": "CatalogOffering",
                    "id": "o0.0",
                    "ProductOptions": [...],
                    "Price": {...},
                    "TermsAndConditions": {...}
                },
                ...
            ]
        },
        "ReferenceList": [
            ...
        ]
    }
}
```