# NEXO Market Monitor — Mobile PWA (interfaz 0.1)

Esta carpeta contiene una **interfaz móvil instalable tipo PWA**, pensada para Android. No es un APK ni una aplicación publicada en Play Store.

## Estado real
- Interfaz móvil adaptable: implementada.
- Manifest y service worker: incluidos.
- Caché básica para abrir la interfaz después de la primera carga: incluida.
- Cotizaciones reales, análisis conectado, noticias, cartera persistente, API y base de datos: **pendientes**.
- No incluye Telegram ni otros canales de alerta.
- No contiene cotizaciones ficticias: la interfaz indica que está en modo demo.

## Cómo publicarla para instalarla en Android
1. Sube el contenido de esta carpeta a un repositorio GitHub.
2. Activa GitHub Pages en Settings → Pages → Deploy from a branch → `main` → `/ (root)`.
3. Espera a que GitHub Pages publique el sitio HTTPS.
4. Abre la URL publicada en Chrome desde Android.
5. Menú ⋮ → `Instalar aplicación` o `Agregar a pantalla principal`.

## Siguiente fase técnica
Para convertirla en un monitor real hace falta un backend HTTPS y una base de datos. GitHub Actions puede ejecutar análisis programados, pero no debe usarse como API permanente ni como base de datos. El backend deberá consultar proveedores con licencia/cobertura adecuada para acciones, ETF e instrumentos mexicanos, normalizar símbolos y marcas de tiempo, calcular indicadores y guardar resultados. La interfaz consumirá ese backend mediante una API autenticada.

## Seguridad
No pongas claves de proveedores dentro de `app.js`, HTML ni el repositorio. Deben vivir en secretos del backend. No conectar cuentas de corretaje ni habilitar órdenes en esta etapa.
