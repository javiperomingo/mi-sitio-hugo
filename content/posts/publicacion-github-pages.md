---
title: "Despliegue de nuestro sitio Hugo en GitHub Pages (PrácticaX2)"
date: 2026-11-05T17:30:00+01:00
draft: false
---
Para publicar nuestro sitio Hugo en **GitHub Pages** bajo la subruta del repositorio (`https://javiperomingo.github.io/mi-sitio-hugo/`), hemos aplicado tres ajustes esenciales:

1. **Configuración de `baseURL` y `publishDir`:** En `hugo.toml` definimos la URL pública final y el directorio de salida para que Hugo genere todas las rutas de forma coherente.
2. **Uso de `relURL` en las plantillas:** En los parciales de cabecera y navegación empleamos `{{ "css/estilo.css" | relURL }}` y `{{ .Site.Home.RelPermalink }}` para evitar enlaces o estilos rotos al servir la web desde un subdirectorio.
3. **Fichero `.nojekyll`:** Añadimos `static/.nojekyll` para que GitHub Pages sirva directamente el HTML plano generado por Hugo sin procesarlo con Jekyll.
