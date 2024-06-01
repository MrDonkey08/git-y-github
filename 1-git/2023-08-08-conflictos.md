---
layout: post
title: Conflictos en Merge
author: Alan Yahir Juárez Rubio
categories:
  - informatica
  - git
tags:
  - merge
  - conflicto
date: 2023-08-08 18:00:00
last_modified_at: 2024-05-31

toc:
  sidebar: right
---

Un **conflicto** al usar **merge** se genera cuando el último **commit** del
**HEAD** y la **rama** señalada modifican la misma línea.

Cuando **git** detecta un **conflicto**, modifica el archivo de la siguiente manera

```txt
...
<<<<<< HEAD
 Lineas modificadas
 del HEAD
 ...
 =======
 Líneas modificadas
 del segundo branch
 ...
>>>>>> nombre del segundo branch
...
```

## Cómo solucionar un conflicto

Para resolver este **conflicto** bastaría con editar el archivo, eliminar lo
que no quieras y agregar o modificar contenido si es necesario. Al final
debería quedar así

```txt
...
 Líneas definitivas
 del merge
...
```

Una vez resuelto todos los **conflictos** solo restaría aplicar un `add` y un
`commit` para que el **merge** sea satisfactorio.

---

<div style="page-break-after: always;"></div>

## Referencias

- [Vega, F.](https://platzi.com/profes/freddier/)
  (mayo 20, 2019).
  [Curso Profesional de Git y GitHub](https://platzi.com/cursos/git-github/).
  [Platzi](https://platzi.com/).
  Recuperado el 10 de agosto de 2023 de
  <https://platzi.com/new-home/clases/1557-git-github/19941-resolucion-de-conflictos-al-hacer-un-merge/>
