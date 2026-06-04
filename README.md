# Super Flash Chicken — Landing Page

Sitio web de una sola página para **Super Flash Chicken**, pollería y delivery ubicada en Balconcillo, La Victoria, Lima. Construido como HTML/CSS/JS puro — sin frameworks, sin dependencias, sin build step.

**Live:** https://biney-debug.github.io/super-flash-chicken/

---

## Stack

| Capa | Tecnología |
|------|-----------|
| Markup | HTML5 semántico |
| Estilos | CSS3 vanilla (variables, grid, flexbox, clip-path, keyframes) |
| Scripts | Vanilla JS (IntersectionObserver, Canvas API, requestAnimationFrame) |
| Fuentes | Google Fonts — Oswald 700/900 + Inter 400/500/600/700 |
| Íconos | SVG inline custom (estilo Lucide/Phosphor) |
| Deploy | GitHub Pages (branch `master`, raíz `/`) |

---

## Estructura

```
super-flash-chicken/
├── index.html
└── assets/
    ├── hero.mp4           # Video de fondo del hero
    ├── logo.jpg           # Logo circular en nav y footer
    ├── favicon.png        # Favicon circular con fondo transparente
    └── combo-2pollos.jpg  # Foto del combo destacado (pendiente)
```

---

## Secciones

| ID | Sección | Descripción |
|----|---------|-------------|
| `#hero` | Hero | Video de fondo, título animado, badge, teléfonos, CTAs hacia WhatsApp |
| `#stats` | Stats bar | S/17 · 3 líneas · 7 días · Delivery — fondo crema, iconos SVG en círculo rojo |
| `#menu` | Carta | Cards de productos con precios y botones "Pedir" directo a WA |
| `#featured` | Combo destacado | Sección 2 Pollos Completo S/109 con imagen y CTA |
| `#delivery` | Cómo pedir | Horario, línea fija, WhatsApp x2, local, Facebook |
| `#contact` | Contacto | Dirección, teléfonos, mapa embed Google Maps |
| — | Footer | Logo circular, copyright, enlace Facebook |
| — | WA float | Botón flotante WhatsApp fijo en esquina inferior derecha |

---

## Funcionalidades

- **Video hero** — `assets/hero.mp4` como fondo con overlay rojo, autoplay, loop, muted, playsinline
- **Navegación sticky** — transparente sobre el hero, fondo crema al hacer scroll (logo 54px, sin encogimiento)
- **Logo circular** — imagen de marca en nav (48px) y footer (40px), border-radius 50%
- **Favicon circular** — PNG con esquinas transparentes generado con Pillow
- **Menú hamburger mobile** — overlay full-screen, botón X, click fuera para cerrar, transición suave
- **Scroll reveal** — cards y secciones animan al entrar al viewport (IntersectionObserver)
- **Partículas** — canvas con sparks animados en el hero
- **Botones WhatsApp** — en cada producto, abren chat directo con mensaje pre-cargado
- **Responsive mobile-first** — breakpoints 768px y 480px, nav con height fijo 56px

---

## Responsive mobile

| Fix | Descripción |
|-----|-------------|
| Nav height | `height: 56px` fijo, sin gaps internos |
| Hero badge | Letra-spacing reducido, `white-space: normal` |
| Hero inner | `width: 100%` en flex container |
| Phone pills | Apiladas verticalmente, ancho completo |
| Btn Pedir | Tap target aumentado a 0.8rem |
| Video | `object-fit: cover` sin escala en portrait |

---

## Contacto del negocio

| Canal | Dato |
|-------|------|
| Línea fija | 01 262-1594 |
| WhatsApp 1 | 935 257 048 |
| WhatsApp 2 | 992 778 940 |
| Dirección | Av. Palermo 405, Balconcillo, La Victoria, Lima |
| Facebook | [Super Flash Chicken](https://www.facebook.com/flashchiken2/) |

---

## Pendiente

- [ ] Agregar horario de atención en sección Delivery (`[HORARIO AQUI]`)
- [ ] Foto real del combo → `assets/combo-2pollos.jpg`
- [ ] Completar card "Más productos" con el resto del menú

---

## Desarrollo local

No requiere servidor. Abre directamente en el navegador:

```
index.html → doble clic o arrastrar a Chrome/Edge
```

Para previsualizar en celular desde la misma red WiFi:

```bash
npx serve . -p 3000
# Luego abre http://<TU_IP_LOCAL>:3000 en el celular
```

---

## Deploy

El sitio se despliega automáticamente en **GitHub Pages** desde el branch `master`.

Flujo para publicar cambios:

```bash
git add index.html assets/   # incluir assets si hay nuevos archivos
git commit -m "fix/feat/style: descripción del cambio"
git push
```

GitHub Pages actualiza en ~1-2 minutos tras el push.

---

## Commits

Formato **Conventional Commits**:

| Tipo | Cuándo usarlo |
|------|--------------|
| `feat` | Nueva sección o funcionalidad |
| `fix` | Corrección de bug visual o funcional |
| `style` | Ajuste de colores, tipografía, espaciado |
| `content` | Cambio de texto, precios, horarios |
| `docs` | Cambios en README u otra documentación |
