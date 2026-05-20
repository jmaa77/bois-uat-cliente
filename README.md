# Bois Bourgeois — Guía de pruebas para clientes (UAT)

Este repo hostea **únicamente** la guía interactiva HTML que el cliente final
usa para probar la app en producción antes del lanzamiento público.

## Para el cliente

Abrí el link que te pasaron por mail o por Drive y seguí la guía.
No tenés que hacer nada con este repo.

## Para el equipo

- Archivo único: `index.html` — la guía self-contained (HTML + CSS + JS + mockups SVG inline).
- Hosteado vía GitHub Pages en `https://jmaa77.github.io/bois-uat-cliente/`.
- Repo público porque GitHub Pages free solo funciona en repos públicos.
- El HTML NO contiene info sensible: es solo una guía con instrucciones y mockups.
- Las respuestas del cliente quedan en SU navegador (localStorage) y se exportan
  como JSON que el cliente comparte por Google Drive — nada se sube acá.

## Actualizar la guía

El "source of truth" del HTML vive en el repo privado principal
(`jmaa77/BoisBourgeois`) en `docs/smoke-tests/uat-cliente-prod.html`.

Para sincronizar una nueva versión a este repo público:

```powershell
copy D:\boisbourgeois\docs\smoke-tests\uat-cliente-prod.html D:\bois-uat-cliente\index.html
cd D:\bois-uat-cliente
git add index.html
git commit -m "chore: sync uat HTML from main repo"
git push
```

GitHub Pages se redeploya automáticamente en ~1-2 minutos.

## Privacidad / seguridad

- ✅ HTML no expone ninguna URL del backend ni credenciales.
- ✅ Cliente carga sus capturas y notas localmente — nunca salen de su navegador
  excepto cuando él clickea "Descargar reporte" (archivo JSON local).
- ✅ Repo no tiene secretos ni código de la app — es solo un HTML estático.
