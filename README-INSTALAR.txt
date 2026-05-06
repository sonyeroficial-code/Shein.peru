APP WEB PWA - VERSION ACTUALIZABLE v93-20260506-actualizable

Archivos principales:
- index.html
- manifest.json
- service-worker.js
- icon-192.png
- icon-512.png
- apple-touch-icon.png
- favicon.png
- .htaccess
- _headers

Que se arreglo:
1. El service worker ahora usa una version nueva de cache.
2. index.html y service-worker.js se piden a la red primero, para que no se quede la version anterior.
3. El registro del service worker usa updateViaCache:'none'.
4. El boton "Actualizar app" borra caches, desregistra el service worker anterior y recarga con parametro nuevo.
5. Se agregaron .htaccess y _headers para hostings que respetan cabeceras de no-cache.

Como subir:
1. Descomprime este ZIP.
2. Sube TODOS los archivos a la misma carpeta de tu hosting, reemplazando los anteriores.
3. Entra a la web y presiona "Actualizar app" desde el perfil.
4. Si ya estaba instalada como PWA, cierra y vuelve a abrir la app.
5. Si aun carga una version vieja, borra datos del sitio o desinstala/reinstala la PWA una sola vez.

Importante:
- En cada nueva version cambia CACHE_VERSION en service-worker.js y APP_UPDATE_VERSION_V93 en index.html.
- Si tu hosting tiene cache/CDN, purga la cache del hosting tambien.
