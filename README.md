# Ficha de Emergencia (FIBE) e Informe ALFA — Ilustre Municipalidad de Castro

Aplicación web de un solo archivo (`index.html`, sin servidor ni compilación) para gestionar eventos de emergencia,
Fichas de Emergencia e Informes ALFA, con exportación a PDF (hoja oficio horizontal, margen 1,27 cm).

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub (ej.: `ficha-emergencia-castro`).
2. Sube estos archivos a la raíz del repositorio: `index.html`, `README.md` y `.nojekyll`.
3. En el repositorio: **Settings → Pages → Build and deployment → Source: "Deploy from a branch"**,
   rama `main`, carpeta `/ (root)` → **Save**.
4. Espera 1–2 minutos: el enlace queda en `https://TU-USUARIO.github.io/ficha-emergencia-castro/`.

Para actualizar la app: reemplaza `index.html` en el repositorio y recarga la página con Ctrl+F5.

## Acceso inicial

- Administrador: usuario `admin`, clave `castro2026`.
- Usuarios nuevos: los crea el administrador (pestaña **Usuarios**). Ingresan con la clave genérica `2026`
  y el sistema les exige crear una clave propia en el primer ingreso.
- Solo el administrador puede crear/cerrar/reabrir eventos, crear usuarios y restablecer claves
  (al restablecer, el usuario vuelve a `2026` y debe crear otra clave propia).

## Importante: limitaciones al alojarlo en GitHub Pages

- **Los datos se guardan en el navegador de cada persona** (localStorage). GitHub Pages no tiene base de datos:
  cada equipo verá solo lo que guardó en su propio navegador. La base de datos compartida en tiempo real
  solo existe cuando la app corre dentro de Claude.
- **El login es un control de acceso básico del lado del navegador**, no una barrera de seguridad real:
  cualquier persona con conocimientos técnicos puede saltárselo. No lo uses para proteger datos sensibles.
- Si borras los datos del navegador se pierden las fichas guardadas. Exporta a PDF lo que necesites conservar.
- Para compartir datos entre usuarios en GitHub se necesitaría conectar la app a un servicio con base de datos
  (por ejemplo Firebase o Supabase); es un trabajo aparte.

## Funciones

Dashboard · eventos (34 tipos, coordenadas GPS→UTM) · fichas de emergencia (con instituciones, 2 fotos y firma
electrónica del encuestador) · informes ALFA · folio correlativo desde 10.00.000 · exportación PDF · instalable como
app en Android (PWA).
