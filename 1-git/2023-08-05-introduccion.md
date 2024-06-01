---
layout: post
title: Introducción a Git
author: Alan Yahir Juárez Rubio
description: Qué es y cómo funciona git y los sistemas de control de versiones

categories:
  - informatica
  - git
tags:
  - control-de-versiones
  - git-lfs
  - binarios-en-git

date: 2023-08-05 10:00:00
last_modified_at: 2024-05-31

mermaid:
  enabled: true
  zoomable: true

toc:
  sidebar: right
---

## Sistema de control de versiones

El **control de versiones** es la práctica de rastrear y gestionar archivos
directorios y sus respectivos cambios.

Por otra parte, un **sistema de control de versiones** es un programa que nos
ayuda a tener un control más práctico y eficiente.

Estos sistemas permiten generan una **base de datos** en la que, por medio de
su interfaz, permiten guardar las modificaciones de tus archivos y registrar
cada versión.

## Git

**Git** es un **sistema de control de versiones** que, en vez de guardar el
archivo completo de cada versión, solo se encarga de guardar los cambios que
hay entre las versiones de los archivos. P. ej:

```mermaid
graph TB

T[almacenamiento.txt] --> Versiones

subgraph Versiones
 direction LR
 subgraph v.1
  direction TB
  t1("Existen dos tipos
   de discos duros:
  HDD y SSD")
 end

 subgraph v.2
  t2["Existen dos tipos
   de almacenamiento:
   HDD y SSD"]
 end

 subgraph v.3
  t3["Existen dos tipos
   de almacenamiento:
   HDD (disco duro)
   y SSD (unidad de
   estado sólido)"]
 end
end

v.1 -- "discos duros
↓
almacenamiento
" --> v.2 -- "
3. -y SSD
3. + (disco duro)

     4. + y SSD (unidad de
     5. + estado sólido)" --> v.3
```

<center>Diagrama del funcionamiento a gran escala de Git</center>

<br>

Como puedes observar, **Git** se encarga de guardar los cambios de una versión
a otra.

## Binarios en Git

Los **archivos binarios**, a diferencia de los de **texto plano**, son aquellos
que, al abrir con el _bloc de notas_ (o cualquier editor de texto plano),
aparecen un montón de símbolos raros, lenguaje que entiende la máquina, pero
nosotros no.

> [!IMPORTANT]
>
> Git solo funciona de esta manera con **texto plano.** Si haces esto con un
> **binario**, tal como un _archivo word_, _no te guardará las modificaciones_,
> en cambio remplazará "la versión anterior" con la "versión actual"; esto impide
> que ahorres espacio y que puedas tener un seguimiento tan eficaz tal como un
> **texto plano**.

En **git** lo ideal sería no trabajar con binarios, sino tenerlos alojados en
otro servicio o servidor (e.g. Google Drive). Sin embargo, si te es
necesario trabajar con _binarios en git_, recomiendo utilizar
[Git LFS](https://git-lfs.com)(_Git Long File System_) ya que permite tratar
a las imágenes como referencias y con ello reducir el tamaño del repositorio,
manteniendo el mismo flujo de trabajo.

<div style="page-break-after: always;"></div>

---

## Referencias

- [Vega, F.](https://platzi.com/profes/freddier)
  (mayo 20, 2019)
  _¿Por qué usar un sistema de control de versiones como Git?_
  [Platzi](https://platzi.com/).
  [Curso Profesional de Git y GitHub](https://platzi.com/cursos/git-github/).
  Consultado el 05 de agosto de 2023 de
  <https://platzi.com/clases/1557-git-github/19934-por-que-usar-un-sistema-de-control-de-versiones-co/>

- Chacon, S. & Straub, B.
  (s.f.)
  _1.1 Getting Started - About Version Control_.
  Consultado el 05 de agosto de 2023 de
  <https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control>

- Atlassian
  (s.f.)
  _¿Qué es el control de versiones?_
  Consultado el 05 de agosto de 2023 de
  <https://www.atlassian.com/es/git/tutorials/what-is-version-control>

  <div style="page-break-after: always;"></div>

---

## Recursos Recomendados

- [Git LFS](https://git-lfs.com/)
