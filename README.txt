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
