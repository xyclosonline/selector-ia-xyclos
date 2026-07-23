# PWA: Selector de Modelo de IA - Xyclos Academy

## Qué es

Progressive Web App (PWA) interactiva que permite elegir el modelo de IA perfecto en 3 preguntas.

## Archivos

- **pwa-selector-ia-index.html** — La app completa (HTML + CSS + JS)
- **pwa-selector-ia-manifest.json** — Configuración de instalación
- **pwa-selector-ia-service-worker.js** — Funcionalidad offline

## Despliegue en Vercel

### Opción 1: CLI (más rápido)

```bash
npm install -g vercel
cd tu-carpeta-pwa
vercel
```

Vercel te pedirá:
- Nombre del proyecto: `selector-ia-xyclos`
- Build settings: Dejar en blanco (no necesita build)
- Output dir: `./` (root)

### Opción 2: GitHub + Vercel (recomendado)

1. Crea un repo en GitHub con estos 3 archivos
2. Ve a vercel.com, conecta tu GitHub
3. Selecciona el repo
4. Deploy automático

## Configuración personalizada

### Cambiar la URL

En **index.html**, si la PWA estará en `selector-ia.xyclos.academy`:

```html
<meta name="start_url" content="/">
```

En **pwa-selector-ia-manifest.json**:

```json
"start_url": "/"
```

### Agregar tu dominio en Vercel

1. Ve a tu proyecto en Vercel
2. Settings → Domains
3. Agrega `selector-ia.xyclos.academy`
4. Apunta tu DNS al CNAME que Vercel te da

## Cómo funciona la PWA

### Instalación

En móvil (iOS o Android):
- Abre la app en el navegador
- Verás un botón "Agregar a pantalla de inicio"
- O: menú → "Instalar app"

En desktop (Chrome, Edge):
- Verás un botón en la barra de dirección
- Haz clic para instalar como app nativa

### Offline

La app funciona sin internet:
- Todos los datos están en el dispositivo
- No requiere conexión para usar el selector
- El service worker cachea todo automáticamente

### Actualización automática

Cada vez que abres la app, Vercel revisa si hay versión más nueva. Si hay cambios, se actualiza automáticamente.

## Enlace desde el blog

En Wix, en el blog "De modelos y tokens", agrega este link:

```markdown
[Abre el selector interactivo](https://selector-ia.xyclos.academy)

o

[Instala la app para elegir tu modelo](https://selector-ia.xyclos.academy)
```

## Seguimiento de uso

Con Vercel Analytics (gratis), puedes ver:
- Cuántas personas usan la app
- Desde dónde acceden
- Dispositivos (móvil vs desktop)

Actívalo en Vercel → Settings → Analytics

## Troubleshooting

### No aparece el botón "Instalar"

- Verifica que el manifest.json esté en la raíz
- Abre con HTTPS (no HTTP)
- Espera 30 segundos, recarga (F5)

### La app no funciona offline

- Verifica que el service-worker.js esté en la raíz
- Abre en incógnito/private (para limpiar cache)
- Recarga (F5)

### Cambios no se ven

- Abre DevTools (F12) → Application → Clear site data
- Recarga (Ctrl+Shift+R)

## Métricas clave para monitorear

Después de 30 días de publicación:

1. **Instalaciones** — ¿Cuánta gente instaló la app?
2. **Uso diario** — ¿Cuántos la abren cada día?
3. **Conversión** — ¿De qué modelo eligen más?
4. **Retención** — ¿Vuelven al día siguiente?

Estos datos te ayudarán a entender si el selector es efectivo y dónde optimizar.

## Contacto y soporte

Si necesitas ajustar:
- Colores: busca `--cian`, `--naranja`, etc. en el HTML
- Recomendaciones: busca `RECOMENDACIONES` en el HTML
- Preguntas: busca `TAREAS`, `DATOS`, `PRESUPUESTO` en el HTML

---

**Versión:** 1.0 | **Fecha:** Julio 2026 | **Creado por:** Xyclos Academy
