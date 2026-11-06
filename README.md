# constanzasitjaabogada.com

Web de Constanza Sitjà, abogada y mediadora en Barcelona. Sitio estático en Jekyll, publicado con GitHub Pages.

## Estructura

| Ruta | Contenido |
|---|---|
| `_config.yml` | Datos de la titular (nombre, NIF, colegiada, dirección, teléfono, correo) y token de Cloudflare Web Analytics |
| `_data/areas.yml` | Áreas de práctica: textos de la portada y de *Ámbito de práctica* |
| `_data/formacion.yml` | Formación académica (página *La firma*) |
| `index.html`, `la-firma.html`, `ambito-de-practica.html`, `contacto.html` | Páginas principales |
| `aviso-legal.md`, `politica-de-privacidad.md`, `politica-de-cookies.md`, `declaracion-de-accesibilidad.md` | Textos legales |
| `_layouts/`, `_includes/` | Plantilla: cabecera, pie, monograma, bloque final de contacto |
| `assets/css/main.css` | Estilos |
| `assets/fonts/` | Tipografías alojadas en el sitio (licencia SIL OFL) |
| `assets/img/` | Retrato, fotos y monograma |

## Cambiar datos

Casi todo lo que cambia con el tiempo está en `_config.yml` (bloque `titular`) y en `_data/`. Los textos legales leen los datos de ahí, así que un cambio de dirección se hace en un solo sitio.

## Antes de publicar

- [ ] Rellenar `nif` y `numero_colegiada` en `_config.yml`
- [ ] Confirmar la dirección (Diagonal 468 o Passeig de Gràcia 21)
- [ ] Pegar el token de Cloudflare Web Analytics en `cloudflare_web_analytics_token`
- [ ] Settings › Pages: publicar desde la rama `main`, carpeta raíz; dominio personalizado `constanzasitjaabogada.com`; activar *Enforce HTTPS*

## DNS (cuando el dominio esté en Dinahosting)

| Tipo | Nombre | Valor |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | constanzasitjaabogada.github.io |

## Probar en local

```
bundle install
bundle exec jekyll serve
```

Y abrir http://localhost:4000
