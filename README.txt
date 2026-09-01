GAMEFIX ONE PAGE

Dominio:
https://gamefix.com.es/
(corregido de http:// a https:// en canonical, og:url, JSON-LD,
robots.txt y sitemap.xml; sin colisión con ningún otro dominio
revisado en esta sesión)

Marca:
GameFix Servicio Técnico Consolas y videojuegos

Teléfono caja de información y botones:
+34 914 46 85 03

Diagnóstico:
GRATUITO

Consolas:
- PlayStation 3
- PlayStation 4
- PlayStation 5
- Xbox 360
- Xbox One
- Xbox Series X
- Xbox Series S
- Nintendo Switch
- Mandos

Incluye:
- Logo e isotipo suministrados
- WhatsApp 24/365
- Recogida
- Atención telefónica
- Google Business
- YouTube
- Cal.com
- Formulario SMTP
- Chatbot n8n con posiciones/z-index consolidados
- Mapa
- SEO One Page
- Secciones específicas de consolas, mandos y averías

Variables SMTP compartidas en Vercel:
SMTP_HOST=cp7124.webempresa.eu
SMTP_PORT=465
SMTP_SECURE=true
SMTP_USER=soporte@kelatos.com
SMTP_PASS=[configurada únicamente en Vercel]
CONTACT_EMAIL=soporte@kelatos.com

El correo no aparece visible en la web; solo se utiliza en /api/contacto.

Google Analytics:
G-04L9ZW2R07

HISTORIAL: el repositorio era multipágina (9 páginas /modelos/ de
consolas y numerosas páginas /servicios/) y se convirtió a one-page;
esas páginas fueron eliminadas en commits anteriores. Como ya no
existen en el sitemap actual, se ha añadido middleware.mjs para
redirigir (301) cualquier URL antigua a la home, evitando 404 en
enlaces indexados o backlinks antiguos. Excluye /api/* y cualquier
ruta con extensión de archivo. Se añadió "@vercel/functions": "^2.0.3"
a package.json como dependencia de esta función.

REVISIÓN (fixes aplicados en esta pasada):
- Ya estaba bien: schema.org LocalBusiness (JSON-LD), sección SEO
  "Guía" (id="sobre-reparacion", enlazada en el menú), menú móvil,
  borde blanco del chat, api/contacto.js con SMTP + nodemailer. No se
  ha tocado ninguno de estos.
- Banner de cookies: no existía. Añadido (Aceptar / Rechazar /
  Política de privacidad → https://kelatos.com/privacy-policy/), con
  diseño apilado a ancho completo en móvil.
- Google Analytics: no existía. Añadido G-04L9ZW2R07.
- Dominio corregido de http:// a https:// (canonical, og:url, JSON-LD,
  robots.txt, sitemap.xml).
- .navcall: el texto largo ("Atención Telefónica 24 horas 365 días")
  deformaba la píldora del menú. Acortado a solo el número
  (+34 914 46 85 03) y añadido white-space:nowrap como salvaguarda.
- H1 de portada reescrito, corto, directo y totalmente afirmativo
  (sin interrogación ni condicionales): "Tu consola no enciende. Aquí
  la diagnosticamos y la reparamos." Tamaño del H1 aumentado:
  clamp(38-57px) → clamp(46-74px) en escritorio, 40px → 48px en móvil.

REVISIÓN ADICIONAL (a petición del cliente, regla general de la familia):
- Quitada la pestaña/etiqueta rotada del hero (.hero-chip o
  .hero-tag) que sobresalía y se solapaba visualmente con la caja de
  información en anchos de tablet/escritorio medio (detectado con
  captura en vivo en AcerTech). Regla para toda la familia: no volver
  a añadir este tipo de elemento decorativo. (La regla CSS .hero-chip
  se deja intacta, sin uso, según práctica habitual de la familia.)

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente):
- H1 repetía la plantilla "Tu X no Y. Aquí Z." usada en varios repos
  ("Tu consola no enciende. Aquí la diagnosticamos y la reparamos.").
  Reescrito en formato imperativo: "Repara tu consola o mando con
  diagnóstico gratis." (8 palabras).
- BUG REAL — dos textos decorativos gigantes sin ninguna reducción de
  tamaño en tablet/móvil: ".problems::after" ("GAMEFIX", 170px) y
  ".repair-art::before" ("JUEGA", 118px). Añadida reducción en tablet
  (100px/70px) y móvil (56px/44px). El badge legible
  ".repair-art::after" ("HDMI · LECTURA · TEMPERATURA · MANDOS ·
  CARGA") no es un watermark, no se ha tocado.
- BUG REAL — el botón CTA de teléfono no tenía icono, a diferencia del
  de WhatsApp. Añadido (verificado con cuidado el cierre de las
  etiquetas </a>: 20 aperturas / 20 cierres).
- BUG REAL — la casilla de política de privacidad existía pero el
  texto no enlazaba a ningún sitio. Añadido el enlace estándar de la
  familia a https://kelatos.com/privacy-policy/, resaltado en azul
  (#0758a8, ya que la paleta de esta web es roja/negra sin ningún tono
  azul existente).
- Añadida franja de aviso de servicio técnico independiente debajo del
  menú (no existía). Aplica aquí porque se reparan consolas de marcas
  concretas (PlayStation/Sony, Xbox/Microsoft, Nintendo Switch).
  Verificado antes que .header no usa display:flex directamente.
- Añadido "Sábados, domingos y días festivos estamos cerrados" debajo
  del horario.
- Verificado sin bugs: .hero-shape es un círculo decorativo sin texto
  (no es .hero-chip); Cal.com ya estaba presente; schema.org ya usaba
  correctamente el único teléfono de este repo; formulario
  correctamente conectado a /api/contacto.

REVISIÓN ADICIONAL (checklist unificado de la familia, a petición del cliente — repo 26/48):
- BUG REAL — enlace de Cal.com desactualizado. Actualizado a
  https://cal.com/kelatos/30min?embed=true&theme=light&attendeePhoneNumber=%2B34&overlayCalendar=true.
- Verificado: el correo soporte@kelatos.com no aparece visible.
- BUG REAL — el mensaje prellenado de WhatsApp decía "¡Hola Kelatos!".
  Corregido a "¡Hola GameFix!".
- Verificado: el menú móvil ya se cerraba correctamente al pulsar un
  enlace.
- Verificado: sin iconos ni imágenes con proporciones fijas
  incorrectas.
- Verificado: el H1 en móvil ya está en 48px.
- BUG REAL — botones del hero (.cta) con border-radius de 16px y sin
  estado hover. Aumentado a border-radius:999px; añadido
  filter:brightness(.88) en wa/pickup (colores sólidos) y relleno
  sólido con var(--red) + texto blanco en el botón de teléfono (fondo
  transparente con borde rojo) al pasar el ratón.
- Verificado: este repo no usa el patrón de franja de insignias bajo
  el H1 (familia Dyson); no aplica la reubicación.
