# AGENTS.md

Instrucciones para agentes de IA que trabajan en este proyecto.

## Estructura del proyecto

- `index.html` — Archivo único con HTML + CSS (Tailwind CDN) + JavaScript vanilla
- `.github/workflows/deploy.yml` — GitHub Actions para despliegue automático a GitHub Pages
- `README.md` — Documentación del proyecto

## Stack

- HTML5 semántico
- Tailwind CSS (CDN via `cdn.tailwindcss.com`)
- Font Awesome 6 (CDN)
- SheetJS (CDN via `cdn.sheetjs.com`) para exportación a Excel
- JavaScript vanilla (sin frameworks)
- localStorage para persistencia de datos

## Convenciones

- Todo el código va en `index.html` (no hay bundler ni build step)
- Usar clases de Tailwind para estilos (no agregar CSS custom salvo sea estrictamente necesario)
- Los IDs de inputs usan camelCase: `salaP`, `salaE`, `hdmP`, `hdmE`, `otrosP`, `otrosE`, `hdoP`, `hdoE`
- Las funciones JS van en un solo bloque `<script>` al final del body
- No agregar librerías externas salvo que sea imprescindible (preferir CDN)

## Funcionamiento

### Contadores
- Array `idsP` = pacientes, `idsE` = elaboraciones
- `changeVal(id, delta)` incrementa/decrementa un valor (mínimo 0)
- `updateTotals()` recalcula totales de pacientes y elaboraciones

### Persistencia
- `saveToLocalStorage()` guarda todos los valores + fecha en `localStorage` bajo clave `controlDiario`
- `loadFromLocalStorage()` restaura valores al cargar la página
- Se ejecuta automáticamente al cambiar cualquier input

### Exportar
- `copyData()` copia texto formateado al portapapeles
- `exportToExcel()` genera archivo `.xlsx` con SheetJS

### GitHub Pages
- Despliegue automático en push a `main`
- Workflow en `.github/workflows/deploy.yml`
- Usa `actions/deploy-pages@v4`

## Comandos útiles

```bash
# Abrir localmente
open index.html

# Ver estado de GitHub Pages
gh api repos/{owner}/{repo}/pages
```
