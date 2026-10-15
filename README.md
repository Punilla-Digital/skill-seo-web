# SEO Web

Habilidad completa de Punilla Digital para auditar, instalar y configurar SEO en sitios nuevos o existentes. Reemplaza la versión básica del repositorio.

## Alcance

- Diagnóstico de indexabilidad, HTTP, redirecciones, enlaces y responsables de metadatos.
- Títulos, descripciones, canonical, encabezados, imágenes y datos estructurados.
- Open Graph y vistas previas al compartir enlaces en Facebook, WhatsApp, Instagram y LinkedIn, según el soporte de cada superficie.
- Creación o corrección de sitemap.xml y robots.txt.
- Favicons, Apple touch icon y manifest cuando corresponda.
- Search Console y Bing Webmaster Tools cuando haya acceso autorizado.
- Integración del trabajo con Web Project, Logo Web Kit y Medición y campañas cuando estén disponibles.

No garantiza posiciones, indexación, aparición del favicon ni tarjetas sociales universales.

## Archivos

- [SKILL.md](SKILL.md): procedimiento completo.
- [references/implementacion.md](references/implementacion.md): adaptación por plataforma, ejemplos de head, sitemap y robots.
- [references/fuentes.md](references/fuentes.md): documentación oficial para revalidar requisitos.
- [agents/openai.yaml](agents/openai.yaml): metadatos de interfaz.
- [assets/icon.svg](assets/icon.svg): icono de la habilidad.

## Uso

Copiar la carpeta completa con el nombre `seo-web` al directorio de skills de un agente compatible. Conservar referencias, metadatos e icono junto a SKILL.md. La publicación en GitHub no instala automáticamente la habilidad en ChatGPT.

Ejemplo:

> Usá SEO Web para revisar este sitio y configurar títulos, canonical, vistas previas sociales, sitemap.xml, robots.txt y favicons.

Proporcionar el proyecto o acceso autorizado, dominio de producción, objetivo y recursos de marca disponibles. Si solo se dispone de capturas, la habilidad guía la configuración sin afirmar que ejecutó cambios.

## Requisitos y límites

No incluye scripts propios: el agente implementa los cambios con las herramientas del proyecto. Necesita inspección del HTML y archivos; consulta de documentación oficial actual para requisitos cambiantes; y herramientas de validación según la tarea. Funciona con HTML, WordPress, Drupal, otros CMS y aplicaciones web, respetando sus generadores y evitando duplicados.

Las herramientas PDF, de imágenes, CMS, cuentas y otras habilidades mencionadas no están incluidas. Search Console, Bing y los inspectores sociales requieren el acceso correspondiente. Separar configuración local, publicación, rastreo e indexación observada.

## Origen

Copia de la habilidad instalada en Complementos, publicada el 15/10/2026. Incluye sus referencias e icono y conserva sus instrucciones. Esta publicación no modifica la habilidad instalada.

[Punilla Digital](https://punilladigital.com.ar/) · [Licencia](LICENSE)
