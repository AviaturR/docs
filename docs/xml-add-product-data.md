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
