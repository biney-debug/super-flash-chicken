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
└── index.html   # Todo el sitio en un solo archivo
```

No hay carpetas de assets aún. Las imágenes pendientes van en:

```
super-flash-chicken/
├── index.html
└── assets/
    └── combo-2pollos.jpg   # Foto del combo destacado (pendiente)
```

---

## Secciones

| ID | Sección | Descripción |
|----|---------|-------------|
| `#hero` | Hero | Título animado, badge, teléfonos, CTAs hacia WhatsApp |
| `#stats` | Stats bar | S/17 · 3 líneas · 7 días · Delivery |
| `#menu` | Carta | Cards de productos con precios y botones "Pedir" directo a WA |
| `#featured` | Combo destacado | Sección 2 Pollos Completo S/109 con imagen y CTA |
| `#delivery` | Cómo pedir | Horario, línea fija, WhatsApp x2, local, Facebook |
| `#contact` | Contacto | Dirección, teléfonos, mapa embed Google Maps |
| — | Footer | Marca, copyright, enlace Facebook |
| — | WA float | Botón flotante WhatsApp fijo en esquina inferior derecha |

---

## Funcionalidades

- **Navegación sticky** con scroll — transparente en hero, sólida al bajar
- **Menú hamburger mobile** con overlay full-screen, botón X, click fuera para cerrar, transición suave
- **Scroll reveal** — cards y secciones animan al entrar al viewport (IntersectionObserver)
- **Partículas** — canvas con sparks animados en el hero
- **Botones WhatsApp** en cada producto — abren chat directo con mensaje pre-cargado
- **Responsive mobile-first** — breakpoints 768px y 480px

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
git add index.html
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
