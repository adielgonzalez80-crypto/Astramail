# CorreoNova V11 — GitHub primero, Cloudflare después

Esta versión conserva el Worker de CorreoNova V10 y prepara el proyecto para trabajar con GitHub como repositorio principal antes de desplegarlo en Cloudflare.

## Estructura

- `correonova_worker.js` — Worker principal existente.
- `README.md` — instrucciones.
- `.gitignore` — archivos que no deben subirse.
- `wrangler.toml.example` — plantilla para el despliegue posterior en Cloudflare.
- `GITHUB_SETUP.md` — pasos para subir el proyecto a GitHub.

## Flujo previsto

1. GitHub: código fuente, historial y copias de seguridad.
2. Desarrollo/pruebas.
3. Cloudflare Workers: ejecución pública.
4. Cloudflare D1/KV/R2: almacenamiento de producción cuando pasemos a correo real.

## Importante

GitHub no debe utilizarse como base de datos para mensajes privados, contraseñas o correos de usuarios. En esta etapa GitHub funciona como repositorio del código. Los datos reales de los usuarios deberán pasar posteriormente a almacenamiento de servidor apropiado.

## Próxima fase

La siguiente implementación debe añadir autenticación, base de datos de usuarios/mensajes y envío/recepción de correo real sin romper la interfaz de CorreoNova.
