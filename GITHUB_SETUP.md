# Subir CorreoNova V11 a GitHub

## 1. Crear el repositorio

Crea un repositorio nuevo en GitHub, por ejemplo:

`CorreoNova`

Para este proyecto conviene que el repositorio sea privado mientras desarrollamos la plataforma.

## 2. Subir estos archivos

Sube:

- `correonova_worker.js`
- `README.md`
- `.gitignore`
- `wrangler.toml.example`
- `GITHUB_SETUP.md`

## 3. Seguridad

No subas:

- contraseñas
- tokens
- claves API
- secretos de Cloudflare
- datos reales de usuarios
- correos privados
- archivos `.env`

## 4. Después de GitHub

Cuando el repositorio esté listo, conectaremos el proyecto con Cloudflare Workers.

El objetivo será:

GitHub → código/versiones → Cloudflare Workers → almacenamiento Cloudflare.

## 5. Base de datos

GitHub será el lugar del código, no la base de datos de los usuarios.

Para producción usaremos posteriormente una opción de Cloudflare apropiada, como D1/KV/R2 según el tipo de información que CorreoNova necesite almacenar.
