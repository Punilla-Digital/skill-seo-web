---
name: seo-web
description: Auditar, instalar y configurar SEO en sitios nuevos o existentes, WordPress, Drupal, otros CMS, HTML y aplicaciones web. Usar para posicionamiento orgánico inicial en Google y Bing, títulos y descripciones, canonical, datos estructurados, enlaces internos, sitemap.xml, robots.txt, favicons y vistas previas al compartir enlaces en Facebook, WhatsApp, Instagram y LinkedIn. Integrar el trabajo con Web Project y Medición y campañas cuando corresponda.
---

# SEO Web

## Misión y forma de trabajo
Implementar SEO verificable, desde la arquitectura hasta la publicación. Responder en español claro y orientar las decisiones al negocio. Ejecutar cambios cuando se tenga acceso autorizado; si solo hay capturas o acceso del usuario, guiar por bloques pequeños con valores listos para copiar. No presentar recomendaciones como instalaciones realizadas ni prometer posiciones, indexación, favicon o previews garantizados por las plataformas.

Leer primero AGENTS.md, Git, documentación, dominio y stack existentes. Identificar producción, staging y demos; respetar cambios ajenos. Relevar audiencia, oferta, zona, idioma, conversión, páginas y marca reales. Preguntar solo datos imprescindibles ausentes. No inventar dominios, textos comerciales, credenciales, IDs, reseñas ni datos de empresa.

Leer [implementación](references/implementacion.md) antes de intervenir y [fuentes](references/fuentes.md) para verificar reglas vigentes de plataformas. Usar documentación oficial actual para tamaños, políticas, límites e interfaces cambiantes.

## 1. Diagnóstico y alcance
- Inventariar URLs, respuestas HTTP, redirecciones, metadatos, encabezados, recursos, enlaces, indexabilidad, sitemap, robots y plugins/módulos existentes. Revisar el HTML inicial y el renderizado cuando corresponda.
- Determinar quién genera cada elemento: CMS, tema, plugin, generador o código. Modificar esa fuente; evitar insertar otro plugin o duplicar title, canonical, JSON-LD y Open Graph.
- Establecer una matriz por URL: propósito, intención de búsqueda, título, descripción, H1, canonical, indexación, imagen social, enlaces y estado. Priorizar bloqueos de rastreo/indexación y errores antes de mejoras editoriales.
- Adaptar el alcance contratado. El antecedente de SEO básico de Punilla Digital fue una optimización inicial de hasta cinco páginas, sin mantenimiento mensual; no imponer ese límite a todos los proyectos.

## 2. Arquitectura, contenido y experiencia
- Definir navegación, URLs legibles, páginas de servicios y enlaces internos útiles entre inicio, servicios, fichas, categorías y blog. Evitar páginas huérfanas y contenido repetido. No cambiar URLs existentes sin mapa de redirecciones permanentes y actualización de enlaces.
- Redactar títulos y metadescripciones únicos, precisos y coherentes con cada página; evitar relleno de palabras clave. Usar longitudes orientativas, sin tratarlas como reglas de ranking ni límites universales.
- Establecer un título principal claro y una jerarquía semántica de encabezados; describir imágenes informativas con alt y usar alt vacío en decoración. Mantener texto y enlaces accesibles en móvil y contenido importante rastreable.
- Revisar velocidad y estabilidad visual, imágenes dimensionadas y comprimidas, carga de fuentes, video y JavaScript. Medir antes/después si se afirma una mejora; no sacrificar contenido o accesibilidad por una puntuación.
- Revisar enlaces rotos, HTTPS, códigos 404/410 reales, redirecciones y página 404 útil. Una página de error visual con HTTP 200 sigue siendo un problema.

## 3. Metadatos y datos estructurados
Configurar charset, idioma real, viewport, title, description y canonical absoluto coherente con HTTPS y el host elegido. Revisar meta robots y X-Robots-Tag juntos. Usar hreflang solo para variantes reales con reciprocidad y códigos válidos.

Agregar JSON-LD apropiado al contenido: Organization o LocalBusiness según entidad real, WebSite, BreadcrumbList y Article/Product cuando corresponda. No fabricar opiniones, precios ni resultados enriquecidos. Validar sintaxis y requisitos del tipo con herramientas oficiales; los datos estructurados no garantizan resultados especiales.

## 4. Vistas previas sociales
Configurar Open Graph por página en el HTML inicial: og:title, og:description, og:type, og:url, og:site_name, og:locale cuando corresponda y og:image absoluto con alt, dimensiones y tipo reales. Añadir Twitter Card si es pertinente. Usar una imagen general de respaldo y específicas para servicios/artículos; no confundir favicon, logo y portada social.

Preparar una imagen social JPG/PNG con marca y texto legibles, composición con margen para recortes; 1200×630 es un punto de partida habitual, sujeto a requisitos vigentes. No publicar rutas de archivos inexistentes. Comprobar HTTP 200, MIME, HTTPS, acceso público sin cookies y bloqueos de CDN/WAF para HTML e imagen. No depender de GTM ni de JavaScript del cliente para generar estos metadatos.

Validar Facebook con Sharing Debugger y LinkedIn con Post Inspector cuando haya acceso. Probar WhatsApp en un chat de prueba autorizado, sin enviar a terceros. En Instagram distinguir mensajes directos, biografía, historias y publicaciones: la superficie y versión de la app determinan si hay tarjeta; Open Graph no obliga a mostrarla. No prometer previews universales. Separar configuración correcta, lectura del bot, caché y comportamiento observado; no afirmar prueba en una app que no se abrió.

## 5. Sitemap y robots
Crear o corregir `sitemap.xml` y `robots.txt` (plural; `robot.txt` no es el archivo estándar). En CMS conservar el sitemap nativo o del plugin si ya funciona y documentar su URL, evitando mapas competidores; usar /sitemap.xml como entrada o alias coherente si se necesita ese nombre.

Incluir en el sitemap solo URLs canónicas, públicas, indexables y con HTTP 200. Excluir demos, administración, búsquedas internas, errores, redirecciones y URLs noindex. Usar URLs absolutas, XML UTF-8 escapado y namespace correcto; lastmod solo si refleja cambios reales. Respetar límites vigentes y dividir con sitemap index cuando haga falta. Mantener su generación al publicar o eliminar contenido, no solo una copia inicial.

Ubicar robots en la raíz de cada origen; un robots de subcarpeta no regula el dominio. Preservar reglas justificadas y evitar bloquear CSS, JS, imágenes sociales o favicons necesarios. Referenciar el sitemap absoluto. No usar robots para ocultar secretos ni como sustituto de noindex: el bot debe poder leer noindex. Para demos, aplicar noindex rastreable o autenticación según necesidad; no publicar bloqueo global de pruebas en producción. Validar grupos específicos de bots además del grupo genérico.

## 6. Favicons y marca
Partir del logo autorizado. Si requiere normalizarlo o generar variantes usar Logo Web Kit disponible, sin convertirlo en dependencia obligatoria. Crear isotipo legible a tamaño pequeño, fondo/contraste apropiados y formatos reales, sin renombrar extensiones.

Servir /favicon.ico de compatibilidad con tamaños internos apropiados (16, 32, 48), un PNG cuadrado de buena resolución (por ejemplo 96×96), apple-touch-icon 180×180 y, si corresponde, manifest con iconos 192/512. Declarar rel="icon" con type y sizes reales; SVG puede ser adicional, conservar PNG/ICO para compatibilidad. No mezclar favicon con og:image.

Verificar declaraciones en el head de la portada y las plantillas, archivos HTTP 200 sin autenticación, MIME, dimensiones, estabilidad de URL y acceso de Googlebot/Googlebot-Image/Bingbot. Revisar robots y WAF. Usar recomendaciones oficiales actuales para Google; para Bing verificar documentación y rastreo, sin inventar una etiqueta exclusiva ni afirmar tamaños obligatorios sin fuente. Distinguir icono visible en navegador de favicon mostrado en Google/Bing: estos últimos requieren rastreo y pueden tardar o elegir otro resultado.

## 7. Indexación y medición
Conectar/verificar Google Search Console y Bing Webmaster Tools con la cuenta y propiedad correctas cuando esté autorizado; conservar verificaciones existentes. Presentar sitemap e inspeccionar URLs representativas, anotando aceptación, descubrimiento e indexación por separado. No afirmar envíos sin evidencia ni usar APIs de indexación fuera de sus tipos admitidos.

Aplicar Medición y campañas para GA4, GTM, Meta Pixel y conversiones solicitadas. Auditar instalaciones primero y evitar duplicados; no copiar IDs de otros clientes. Diferenciar configuración SEO de analítica/publicidad: el Pixel no es requisito para tarjetas sociales ni mejora el ranking. No agregar publicidad con gasto por una solicitud de SEO. Preparar medición de consultas, impresiones, clics y páginas en Search Console; eventos de negocio en la herramienta apropiada.

## 8. Validación, documentación y entrega
Validar inicio, páginas interiores y tipos de contenido con evidencia real: HTML inicial, títulos únicos, canonical, HTTP, XML, robots, JSON-LD, iconos, imágenes, móvil y enlaces. Usar herramientas disponibles y describir límites de acceso; si falta producción, separar verificación local de pública. No declarar indexado por haber creado un sitemap.

Con Web Project, integrar matriz SEO, resultados, feedback y pendientes en la documentación existente (por ejemplo docs/seo/), sin reorganizar el repositorio por obligación. Registrar fuente modificada, URL, comprobación, fecha y estado: preparado, instalado, probado, publicado o pendiente. Mantener demos fuera del mapa de producción y revisar noindex al lanzar. Respetar autorización de publicación ya recibida.

Entregar resumen breve de resultados, páginas intervenidas, URLs de sitemap/robots, archivos de favicon y portada, pruebas reales y pendientes externos. Usar tabla cuando ayude. En explicaciones comerciales priorizar beneficios y omitir detalles innecesarios; incluir detalles técnicos cuando el usuario los pida. Commit de cambios del proyecto si está autorizado, sin archivos ajenos ni secretos.
