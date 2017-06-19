+++
title = "Como escribir un post para dev/upao"
author = "/dev/ali"
date = "2017-06-19"
description = "Como escribir un post para dev/upao"
tags = ["hugo", "github", "dev/upao"]
+++

Gracias por leer este artículo, entiendo que deseas colaborar con la comunidad de Dev/UPAO.  El blog de Dev/UPAO está hecho por desarrolladores para desarrolladores, actualmente está desplegado sobre github.io, el cual es un proveedor de páginas estáticas, o sea html puro.

## ¿Qué es GitHub Pages?
#TODO
## ¿Que es un generador de páginas estáticas?
#TODO
### ¿Quien es HUGO?
## Ventajas:
- Nos permite trabajar con hostings estáticos.
- Trabaja con **Markdown**
- Es fácil de instalar y usar.
## ¿Como enviar mi post?
Para enviar tu post como un buen **desarrollador alpha** tienes que enviar un `pull request` a nuestro repositorio [GitHub - DevUPAO/devupao.github.io-src](https://github.com/DevUPAO/devupao.github.io-src)  con tu post en la carpeta `/content/post`

### Conocimientos requeridos
<i class="fa fa-check"></i>  Git

<i class="fa fa-check"></i>  Markdown

### Método 1: Realizando un Clone

La primera forma es hacer un clone de la página de devupao localmente
```
git clone git@github.com:DevUPAO/devupao.github.io-src.git
```

Ejecutan hugo para crear un nuevo post donde `first-post.md` es el nombre de tu post

```bash
hugo new post/first-post.md
```

> Para los usuarios de Windows, se ha incluido un `hugo.exe` en el repositorio el cual facilita la ejecución con `hugo.exe new post/first-post.md`  

Modifican el archivo creado en `content/post/first-post.md`.

Para ver el post que han escrito, ejecutan `hugo server -w` el `w` hará que el servidor se actualice con `livereload` o sea mientras actualizan el archivo.


Luego hacen:
```
git add -A
git commit -m "Mi Primer Post"
git push origin your-post
```

Luego te vas a tu repositorio en github y haces un `pull request`, con ello enviarás tu publicación a dev/upao, nosotros lo validaremos e integraremos a nuestro repositorio y por lo tanto a la página.

### Método 2: Creando y editando el archivo directamente en github.
#Todo
- - - -
### Adicional: Estructura del post

```
---
author: "Juan Perez"
date: 2017-06-19
title: Hola Mundo
description: Todo el mundo tiene un hola mundo
tags: "etiqueta1", "etiqueta2", "etiqueta3"
---

## Sub titulo
```

Si tienes alguna pregunta, no dudes en escribirnos a  [la fanpage de la comunidad](https://www.facebook.com/Devupao-450137858679179/).