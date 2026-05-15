# Web Anachi

Landing page corporativa de Aduanas Anachi, una agencia de aduanas en Las Palmas de Gran Canaria especializada en gestión aduanera, operaciones de importación/exportación, mercancías REA, alimentación y bebidas.

## Stack

- Astro 6
- Tailwind CSS 4
- `@astrojs/vercel` para despliegue en Vercel
- `pnpm` como único gestor de paquetes

## Estructura

```text
/
├── public/
│   └── favicon.svg
├── src/
│   ├── assets/
│   │   ├── about.png
│   │   ├── hero-bg.png
│   │   ├── logo.png
│   │   └── logo-dark.png
│   ├── components/
│   │   ├── AboutSection.astro
│   │   ├── ContactSection.astro
│   │   ├── Footer.astro
│   │   ├── Header.astro
│   │   ├── HeroSection.astro
│   │   ├── ServiceSection.astro
│   │   └── SocialSection.astro
│   ├── layouts/
│   │   └── Layout.astro
│   ├── pages/
│   │   └── index.astro
│   └── styles/
│       └── global.css
├── astro.config.mjs
├── tailwind.config.mjs
├── tsconfig.json
├── package.json
└── pnpm-lock.yaml
```

## Secciones

- Cabecera con navegación desktop, menú móvil y llamada a contacto.
- Hero principal con imagen de fondo y propuesta de valor.
- Bloque de confianza con contadores de experiencia, clientes y despachos.
- Servicios aduaneros en tarjetas.
- Sección de empresa con historia, credenciales OEA y equipo.
- Contacto con dirección, teléfonos, emails, formulario Formspree y FAQ.
- Footer con navegación, datos de contacto y LinkedIn.

## Comandos

Ejecuta todos los comandos desde la raíz del proyecto.

| Comando | Acción |
| :-- | :-- |
| `pnpm install` | Instala dependencias |
| `pnpm dev` | Arranca el servidor local en `localhost:4321` |
| `pnpm build` | Genera la build de producción en `dist/` |
| `pnpm preview` | Previsualiza la build localmente |
| `pnpm astro ...` | Ejecuta comandos de Astro CLI |

## Desarrollo

- No uses npm ni yarn en este repositorio.
- No generes ni subas `package-lock.json`.
- Los estilos globales y variables de marca están en `src/styles/global.css`.
- Los anchors principales son `#home`, `#services`, `#about-us` y `#contact`.
- El formulario de contacto usa Formspree desde `src/components/ContactSection.astro`.
- Ejecuta `pnpm build` antes de considerar terminados los cambios.

## Despliegue

El proyecto está configurado con `@astrojs/vercel`. La salida de producción se genera en `dist/` y los artefactos de Vercel en `.vercel/`; ambos son generados y no deben versionarse.
