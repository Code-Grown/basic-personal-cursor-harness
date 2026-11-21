# Piso frontend común (método)

Estándar mínimo para las páginas y portales de CodeGrown. Vive una vez en el hub. Cada repo apunta a este piso y solo agrega lo propio: tipo de sitio y su manual de tokens.

## Piso (toda página o portal)
- Accesibilidad WCAG 2.2 AA: contraste 4,5:1 en texto y 3:1 en componentes; reflow a 320 px; teclado y foco visible; alt en imágenes; labels en formularios; objetivos táctiles de 24 px o más. Es piso de calidad en todos; la obligación legal (Ley 21.180 y su norma técnica) aplica cuando el cliente es del Estado.
- Core Web Vitals en verde, medidos en móvil: LCP < 2,5 s, CLS < 0,1, INP < 200 ms. Imágenes en webp o avif con tamaño declarado; video liviano con poster.
- Mobile first: se revisa a 390 px antes que a 1440 px, sin scroll horizontal.
- Seguridad y datos: HTTPS; aviso de privacidad y consentimiento explícito si se recogen datos personales (Ley 19.628 y Ley 21.719). Nada de secretos en el frontend.
- SEO técnico básico en sitios públicos: title y description únicos, canonical, sitemap.xml, robots.txt, Open Graph y noindex donde corresponda.
- Usabilidad: estados de carga, error y vacío; mensajes en lenguaje claro; consistencia.

## Según el propósito (solo lo que aplique)
- Landing de campaña: un objetivo y un CTA; sin menú que distraiga; mensaje alineado al anuncio; poco texto; formulario corto; UTM, gclid, gbraid y wbraid guardados junto al lead.
- Web institucional o SEO: arquitectura por servicios, contenido indexable, navegación clara.
- Portal o app con login: flujos clic a clic (login, panel, salida); roles y permisos; sesiones seguras.
- Marca: cada producto tiene su propio manual de tokens y no hereda el de otro.

## Cómo entra en un pitch
En un cambio de UI, «listo cuando» incluye siempre axe sin errores serios y capturas a 390 y 1440 px. Lighthouse móvil (90 o más en Performance y Accessibility) solo si el cambio puede mover LCP, CLS o INP. CI con Lighthouse CI y axe: al principio avisa y no bloquea. Se audita lo que ya está en producción y se arregla en pitches chicos, sin rediseños grandes.
