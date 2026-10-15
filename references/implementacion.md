# Implementación y ejemplos

## Selección por plataforma
- HTML estático: editar templates/fuentes y generador; regenerar y verificar todas las páginas, no solo el HTML generado de inicio.
- WordPress: identificar plugin SEO activo, ajustes de lectura, tema y sitemap; no instalar dos responsables SEO. Revisar salida de wp_head, icono del sitio, cache y redirecciones. Preferir APIs, child theme o plugin específico a tocar el núcleo.
- Drupal: detectar versión y módulos existentes para metadatos, canonical, sitemap y redirecciones; no asumir compatibilidad entre Drupal 7 y moderno. Evitar modificar core y limpiar la caché correspondiente.
- Laravel, SSR y aplicaciones JS: usar layout/head del servidor por ruta o prerender estático apropiado. Verificar respuesta sin ejecutar JS y ausencia de metadatos duplicados tras hidratar. No insertar SEO crítico mediante GTM.

## Ejemplo de head
Ejemplo ficticio: sustituir todos los datos y crear los recursos antes de publicarlo. El tipo, locale y contenido dependen de la página.

```html
<title>Servicio específico | Marca</title>
<meta name="description" content="Descripción real y particular del servicio.">
<link rel="canonical" href="https://example.com/servicio/">
<meta property="og:type" content="website">
<meta property="og:title" content="Servicio específico | Marca">
<meta property="og:description" content="Descripción real del servicio.">
<meta property="og:url" content="https://example.com/servicio/">
<meta property="og:site_name" content="Marca">
<meta property="og:locale" content="es_AR">
<meta property="og:image" content="https://example.com/media/servicio-social.jpg">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
<meta property="og:image:type" content="image/jpeg">
<meta property="og:image:alt" content="Descripción de la portada del servicio">
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Servicio específico | Marca">
<meta name="twitter:description" content="Descripción real del servicio.">
<meta name="twitter:image" content="https://example.com/media/servicio-social.jpg">
<link rel="icon" href="/favicon.ico" sizes="16x16 32x32 48x48" type="image/x-icon">
<link rel="icon" href="/favicon-96.png" sizes="96x96" type="image/png">
<link rel="apple-touch-icon" href="/apple-touch-icon.png" sizes="180x180">
```

Escapar atributos HTML, serializar JSON-LD con seguridad y construir URLs desde el dominio de producción. No copiar example.com a un cliente. Para despliegues en subcarpetas resolver rutas de recursos según su ubicación real, manteniendo robots en la raíz del origen.

## Sitemap mínimo
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url><loc>https://example.com/</loc></url>
  <url><loc>https://example.com/servicio/</loc></url>
</urlset>
```

## Robots público mínimo
Ejemplo para un sitio completamente público; fusionar con reglas reales, no sobrescribirlas a ciegas.
```text
User-agent: *
Disallow:
Sitemap: https://example.com/sitemap.xml
```

## Comprobaciones prácticas
- Comparar GET y HTML inicial con navegador renderizado; revisar cabeceras HTTP y destino final de redirecciones.
- Comprobar archivos con parsers XML/JSON y dimensiones reales de imágenes/iconos; no basta validar extensión.
- Hacer muestreo representativo de tipos de página y búsqueda global de duplicados o referencias de staging.
- Validar Rich Results Test para tipos compatibles y Schema Markup Validator para vocabulario; no confundir sintaxis correcta con elegibilidad.
- Consultar PageSpeed Insights o mediciones locales reales si se dispone; informar condiciones y fecha, sin inventar puntajes.
- Registrar sin enviar mensajes a terceros las previews que pueden verificarse, y marcar las restantes pendientes.

## Antecedentes incorporados
Historial recuperado el 15/10/2026: optimización de sitios existentes WordPress/CMS/personalizados, arquitectura, rendimiento y móvil; metadatos, JSON-LD y enlaces entre servicios/blog/categorías; integración con Search Console, Analytics, GTM y Meta Pixel; documentación por etapas y demos noindex. Aplicar los aprendizajes generales sin trasladar datos, IDs ni marcas de clientes. El SEO empieza desde el desarrollo. El alcance comercial de cinco páginas fue un caso de servicio básico, no una restricción técnica.
