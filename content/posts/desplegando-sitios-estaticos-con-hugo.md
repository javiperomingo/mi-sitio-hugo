---
title: "Cómo organizar plantillas, parciales y contenido en Hugo"
date: 2026-10-30 12:30:00
draft: false
---

En esta segunda entrada repasamos la arquitectura que hemos montado en nuestro proyecto de Hugo durante la práctica **P1.2 de IAW**:

1. **Contenido en Markdown (`content/`)**: separamos la información (`_index.md`, `contact.md`, `about.md` y la sección `posts/`) del diseño visual.
2. **Parciales reutilizables (`layouts/partials/`)**: extraemos la cabecera (`header.html`) y el pie de página (`footer.html`) para incluirlos mediante `{{ partial "header.html" . }}` y `{{ partial "footer.html" . }}` sin duplicar código HTML.
3. **Vistas de sección (`layouts/section.html`) y de página (`layouts/page.html`)**: automatizamos el listado de artículos del blog con `{{ range .RegularPages }}`.
