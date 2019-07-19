<!-- [![Documentation Status](https://readthedocs.org/projects/polkadot-wiki/badge/?version=latest)](https://polkadot-wiki.readthedocs.io/en/latest/?badge=latest)
[![CircleCI](https://circleci.com/gh/w3f/polkadot-wiki.svg?style=svg)](https://circleci.com/gh/w3f/polkadot-wiki) -->

# Manual de usuario de Kusama

Este repositorio contiene los archivos de origen para la [Guía del usuario de Kusama](https://guide.kusama.network).

## Corriendo localmente

Tenga en cuenta que necesitará el administrador de paquetes `pip`, que generalmente se instala con Python.

Clone el repositorio a su sistema de archivos local.

```bash
git clone https://github.com/kusamanetwork/userguide.git
```

Instale `mkdocs` utilizando el administrador de paquetes `pip`.

```bash
pip install mkdocs --user
```

Ahora instale todas las dependencias necesarias, una vez más usando `pip`.

```bash
pip install -r requirements.txt
```

Ejecute `mkdocs` desde la raíz del repositorio para generar un servidor de desarrollo de recarga en caliente y navegue a `localhost:8000` en un navegador web.

## Publicación

La wiki está alojada en [Read the Docs](https://readthedocs.org) y se basa en cada confirmación publicada en la rama maestra en el repositorio de GitHub.

## Estilo

[Mkdocs-Material](https://squidfunk.github.io/mkdocs-material/) se utiliza para dar a la wiki su tema elegante.

## Contribuyendo

Lea las reglas de contribución en el documento [CONTRIBUYENDO](CONTRIBUTING.md).

### Configuración del colaborador

Como colaborador, deberá ejecutar `npm i` en la copia local de su repositorio después de desactivarlo.

### Añadiendo una nueva página

Si agrega una página, asegúrese de darle la ubicación correcta en la navegación ingresándola manualmente en `mkdocs.yml` debajo del campo de `nav`. Se realiza de esta manera para tener un mayor control sobre cómo se muestran las páginas en la interfaz de usuario y dar mejor organización a los temas.

### Corrección ortográfica

Establecimos ganchos [`husky`](https://github.com/typicode/husky) para detectar errores de ortografía. Si se le está impidiendo que se comprometa, simplemente ejecute  `npm run spellcheck:interactive` para usar el depurador interactivo y corregir su ortografía.
