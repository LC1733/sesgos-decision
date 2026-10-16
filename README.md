# Matriz de Sesgos en la Decisión

PWA de un solo archivo (instalable, funciona sin conexión) con 18 sesgos cognitivos de Kahneman & Tversky organizados en las tres fases de una decisión — percepción del problema, evaluación de opciones, ejecución y revisión — más seis sesgos adicionales, un mapa de flujo fase → sesgo y un autodiagnóstico por fase.

- Sitio: https://lc1733.github.io/sesgos-decision/
- Forma parte del hub **Mente & Decisión**: https://lc1733.github.io/
- Salto directo a sección: `#flow-svg`, `#quiz-section`, `#phases`, `#extra-grid`.
- `catalog.json` describe la app para el hub (convención nivel B).

## Cómo está empaquetada
`index.html` es un cargador: descarga los nueve `app*.b64`, los concatena, decodifica base64 y descomprime gzip, y escribe el HTML resultante en el documento. El `service-worker.js` cachea el shell completo para uso offline. Para editar la app, reconstruye el HTML (`cat app*.b64 | base64 -d | gunzip`), modifícalo y vuelve a comprimir/partir; o abre el sitio, copia el `outerHTML` desde las herramientas de desarrollador y trabaja sobre ese archivo.
