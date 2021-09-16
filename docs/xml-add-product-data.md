---
title: Xml add product data
slug: /xml-add-product-data
---

## Introducción

El xml de addProductData que se genera al crear una transacción

Tag de cliente:

```xml
<client>
  <!--id es obligatorio para procesar transacción-->
	<id>725186</id><!--Numero identificador de cliente en relacionados-->
	<name>Yared</name>
	<last_name>Toro</last_name>
</client>
```

Datos de conexión (desconocido):

```xml
<connection_data>
	<ip>127.0.0.1</ip>
	<loc>{connection_data_loc}</loc>
	<country>{connection_data_country}</country>
	<city>{connection_data_city}</city>
	<connection_info>{connection_data_info}</connection_info>
</connection_data>
```

## resultado del consumo


```xml
<NS1:Envelope xmlns:NS1="http://schemas.xmlsoap.org/soap/envelope/">
    <NS1:Body>
        <NS1:mbus xmlns:NS1="http://www.aviatur.com/soa/formato/mbus/response/version/1.0">
            <NS1:response>
                <NS1:header>
                    <NS1:service>CREA_SOLICITUD_PRODUCTO</NS1:service>
                    <NS1:invoker>BPM</NS1:invoker>
                    <NS1:provider>dummy|http://www.aviatur.com.co/dummy/</NS1:provider>
                    <NS1:requestId>1</NS1:requestId>
                </NS1:header>
                <body>
                    <RESULTADO>EXITO</RESULTADO>
                    <MENSAJE>15982873 - 34934027</MENSAJE>
                </body>
            </NS1:response>
        </NS1:mbus>
    </NS1:Body>
</NS1:Envelope>
```


## Endpoint producción

- https://ecomm5.grupoaviatur.com:8443/Ivunpsoa/bp1.aspx
