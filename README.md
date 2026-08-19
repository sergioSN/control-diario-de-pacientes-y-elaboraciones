# Control Diario de Pacientes y Elaboraciones

Aplicación web de gestión y recuento diario para servicios hospitalarios. Aplicación web de gestión y recuento diario para servicios hospitalarios.

**GitHub Pages:** [https://sergiosn.github.io/control-diario-de-pacientes-y-elaboraciones/](https://sergiosn.github.io/control-diario-de-pacientes-y-elaboraciones/)

## Funcionalidades

- **Selector de fecha** nativo para el turno del día
- **Contadores** por servicio (Sala, HDM, Otros, HDO) con botones +/-
- **Totales automáticos** de pacientes y elaboraciones
- **Persistencia automática** en localStorage del navegador
- **Copiar resumen** al portapapeles en texto formateado
- **Exportar a Excel** (.xlsx) con SheetJS
- **Reiniciar turno** para poner contadores a 0

## Servicios

| Servicio | Pacientes | Elaboraciones |
|----------|-----------|---------------|
| Sala | Contador directo | Contador directo |
| H.D.M. | Contador individual | Contador individual |
| Otros | Recuento externo | Recuento externo |
| H.D.O. | Hoja de registro | Hoja de registro |

## Uso

1. Seleccionar la fecha del turno
2. Incrementar/decrementar contadores con +/-
3. Los datos se guardan automáticamente
4. Al finalizar: copiar resumen o exportar Excel
5. Reiniciar turno para el siguiente

## Despliegue

Se despliega automáticamente a GitHub Pages al hacer push a la rama `main` mediante GitHub Actions.
