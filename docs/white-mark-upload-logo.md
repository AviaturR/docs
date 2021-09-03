---
title: Servicio de cargue de logo
slug: /white-mark-upload-logo
---

## Introducción

El servicio de cargue de logotipo esta diseñador para subir imágenes en la carpeta de assets de marcas blancas para su personalización.

Ruta en el proyecto

- `/web/assets/whitemark_assets/img/header`

```shell
├── web
│   └── assets
│       ├── whitemark_assets
│           ├── img
│               ├── header
```

El funcionamiento del servicio en HXR con js:

```js
var data = new FormData();
data.append("image", fileInput.files[0], "/C:/Users/yared.toro/Downloads/logo-latintravels.png");

var xhr = new XMLHttpRequest();
xhr.withCredentials = true;

xhr.addEventListener("readystatechange", function() {
  if(this.readyState === 4) {
    console.log(this.responseText);
  }
});

xhr.open("POST", "http://mayoristas.grupoaviatur.com/wm-upload-image");
xhr.setRequestHeader("Content-Type", "application/json");
xhr.setRequestHeader("Cookie", "device_view=full");

xhr.send(data);

```

El funcionamiento del servicio en AXIOS con js:

```js
var axios = require('axios');
var FormData = require('form-data');
var fs = require('fs');
var data = new FormData();
data.append('image', fs.createReadStream('/C:/Users/yared.toro/Downloads/logo-latintravels.png'));

var config = {
  method: 'post',
  url: 'http://mayoristas.grupoaviatur.com/wm-upload-image',
  headers: {
    'Content-Type': 'application/json',
    'Cookie': 'device_view=full',
    ...data.getHeaders()
  },
  data : data
};

axios(config)
.then(function (response) {
  console.log(JSON.stringify(response.data));
})
.catch(function (error) {
  console.log(error);
});

```
