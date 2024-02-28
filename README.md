# Hugo Static Sites

Sitios estáticos construidos con el framework Hugo.

- `about_me` Sitio personal en GitHub. Utiliza el tema *Mini*. [🔗](https://lmtreser.github.io/)
- `boards` Sitio del repositorio "boards". Utiliza el tema *Geekdocs*. [🔗](https://lmtreser.github.io/boards/)
- `pcb_libs` Sitio del proyecto "PCB Libs". Utiliza el tema *PaperMod*. [🔗](https://lmtreser.github.io/pcb_libs/)

## Sobre Hugo

Hugo es un generador de sitios estáticos escrito en [Go](https://go.dev/), creado por Steve Francia. Desde el 2015 ha visto un gran incremento en funciones y rendimiento, gracias al desarrollador Bjørn Erik Pedersen (desde v0.14), y otros colaboradores. [Wikipedia](https://es.m.wikipedia.org/wiki/Hugo_(software)).

## Uso

Instalar Hugo en Ubuntu (otros sistemas operativos consultar [Installation](https://gohugo.io/installation/)):

```bash
sudo apt install hugo
```

Crear un nuevo sitio:

```bash
hugo new site nombre_del_sitio
```

Agregar contenido:

```bash
hugo new content posts/my-first-post.md
```

Desplegar el servidor de desarrollo:

```bash
hugo server -D
```

Publicar el sitio:

```bash
hugo
```


## Recursos

- [Hugo](https://gohugo.io/)
- [Hugo Getting Started](https://gohugo.io/getting-started/quick-start/)
- [How to choose the right static site generator](https://about.gitlab.com/blog/2022/04/18/comparing-static-site-generators/)
- [PaperMod Theme](https://adityatelange.github.io/hugo-PaperMod)
- [Even Theme](https://hugo-theme-even.netlify.app/)
- [LoveIt Theme](https://hugoloveit.com/)
- [Mini Theme](https://nodejh.com/hugo-theme-mini/)
- [Geekdocs Theme](https://geekdocs.de/)

## Licencia

Hugo y los temas utilizados están protegidos por sus respectivas licencias. 

Este trabajo está protegido por la **Licencia MIT**. Puedes acceder a la versión original de la licencia (en inglés) a través del archivo [LICENSE](./LICENSE) o en línea en [The MIT License (MIT)](https://mit-license.org/). También proporcionamos una traducción no oficial desde [Wikipedia](https://es.m.wikipedia.org/wiki/Licencia_MIT#La_licencia):

Copyright (c) 2024 Lucas Martín Treser

Por la presente se concede permiso, libre de cargos, a cualquier persona que obtenga una copia de este software y de los archivos de documentación asociados (el "Software"), a utilizar el Software sin restricción, incluyendo sin limitación los derechos a usar, copiar, modificar, fusionar, publicar, distribuir, sublicenciar, y/o vender copias del Software, y a permitir a las personas a las que se les proporcione el Software a hacer lo mismo, sujeto a las siguientes condiciones:

El aviso de copyright anterior y este aviso de permiso se incluirán en todas las copias o partes sustanciales del Software.

EL SOFTWARE SE PROPORCIONA "COMO ESTÁ", SIN GARANTÍA DE NINGÚN TIPO, EXPRESA O IMPLÍCITA, INCLUYENDO PERO NO LIMITADO A GARANTÍAS DE COMERCIALIZACIÓN, IDONEIDAD PARA UN PROPÓSITO PARTICULAR E INCUMPLIMIENTO. EN NINGÚN CASO LOS AUTORES O PROPIETARIOS DE LOS DERECHOS DE AUTOR SERÁN RESPONSABLES DE NINGUNA RECLAMACIÓN, DAÑOS U OTRAS RESPONSABILIDADES, YA SEA EN UNA ACCIÓN DE CONTRATO, AGRAVIO O CUALQUIER OTRO MOTIVO, DERIVADAS DE, FUERA DE O EN CONEXIÓN CON EL SOFTWARE O SU USO U OTRO TIPO DE ACCIONES EN EL SOFTWARE.
