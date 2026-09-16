# Animated UI Theme Pack

A production-quality developer showcase and reference design system demonstrating advanced, practical usage of **CSS Custom Properties (`var(--property)`)**, **Keyframe Animations (`@keyframes`)**, **UI Transitions**, and **GPU-Accelerated 2D Transformations**.

Built strictly using **HTML5 and Modern CSS3** with **zero JavaScript**, zero preprocessors, and zero runtime dependencies. Designed to open directly in any modern web browser.

---

## Live Preview & Overview

The **Animated UI Theme Pack** functions as an interactive developer showcase and component library. Rather than treating animations as mere decorative gimmicks, every motion curve, elevation transition, and 2D transformation is parameterized into a centralized CSS design-token system.

### Core Objectives
1. **Tokenized Design System**: Centralize all colors, typography, spacing, corner radii, elevation shadows, and animation timings into CSS variables.
2. **Motion Architecture**: Standardize reusable keyframe animations and 2D transforms (`translate`, `scale`, `rotate`, `skew`) with dedicated cubic-bezier easing tokens.
3. **Interactive Components**: Showcase buttons, cards, toasts, loaders, badges, and status beacons built with smooth CSS state changes (`:hover`, `:active`, `:focus-visible`).
4. **Pure CSS Theme Switching**: Demonstrate dynamic visual system re-theming using pure CSS variable scoping and sibling pseudo-class selectors.
5. **Accessibility by Default**: Support WCAG contrast guidelines, visible keyboard navigation rings, and automated OS-level `prefers-reduced-motion` compliance.

---

## Features

- ⚡ **Zero Dependencies**: Pure HTML5 and CSS3—no JS runtime overhead or build steps required.
- 🎨 **Centralized Design Tokens**: 30+ reusable CSS custom properties governing color palettes, typography, spacing scales, and shadow elevations.
- 🎛️ **Pure CSS Theme Studio**: Live interactive theme switcher toggling between *Cyber Indigo*, *Emerald Forest*, *Neon Cyberpunk*, and *Sunset Amber* without JavaScript.
- 🎚️ **2D Transform Playground**: Hands-on interactive coordinate lab demonstrating `translate()`, `translateX()`, `translateY()`, `scale()`, `rotate()`, and `skew()`.
- 🎞️ **Reusable Keyframe Gallery**: Visual gallery of 8 standardized keyframes (`fade-in`, `slide-up`, `slide-in`, `pulse`, `float`, `shimmer`, `spin`, `bounce`).
- 🃏 **6 Animated Card Variations**: Dedicated cards demonstrating Lift, Spring Scale, Subtle Tilt, Ambient Glow, Gradient Flow, and Pseudo-Element Reveal.
- 🔘 **Multi-Variant Button Matrix**: Primary, Secondary, Outline, Ghost, Success, Danger, and Disabled buttons with micro-lift and press-down states.
- 📦 **Reusable UI Components**: Live pulsing badges, toast notifications, dual-ring spinners, staggered wave dots, skeleton shimmer loaders, and status beacons.
- 📱 **Mobile-First & Responsive**: Fluid typography via `clamp()`, flexible CSS Grid auto-fit layouts, and responsive media queries covering 320px to 4K.
- ♿ **Inclusive Motion Handling**: Full support for `prefers-reduced-motion: reduce` protecting users with vestibular motion sensitivity.

---

## Technologies Used

- **HTML5**: Semantic document layout (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`).
- **CSS3**: Modern specification features including Custom Properties, `@keyframes`, 2D Transforms, Transitions, `clamp()`, Flexbox, and CSS Grid.

---

## Concepts Demonstrated

| Concept | Implementation Details |
| :--- | :--- |
| **CSS Custom Properties** | Centralized in `:root` and scoped dynamically for theme variations with `var(--token)`. |
| **UI Transitions** | Subtle multi-property transitions (`transform`, `box-shadow`, `border-color`, `opacity`). |
| **2D Transforms** | GPU-accelerated `translateY(-2px)`, `scale(1.03)`, `rotate(1.5deg)`, `skew(-10deg, 4deg)`. |
| **Keyframe Animations** | Standardized `@keyframes` for continuous floats, pings, spins, shimmers, and waves. |
| **Fluid Typography** | Dynamic typography using `clamp(min, preferred, max)` scales. |
| **Modern Layouts** | Resilient CSS Grid (`repeat(auto-fit, minmax(...))`) and Flexbox alignments. |
| **Keyboard Accessibility** | Dedicated `:focus-visible` styling with high-contrast outlines for keyboard users. |
| **Reduced Motion** | Graceful animation neutralization via `@media (prefers-reduced-motion: reduce)`. |

---

## Project Structure

```text
Animated-Ui-Theme-Pack/
│
├── index.html                  # Semantic, accessible UI dashboard markup
│
├── css/
│   ├── style.css               # Main bundle importing all modular layers
│   ├── variables.css           # Central design tokens, color scales & theme overrides
│   ├── base.css                # CSS reset, typography defaults & layout utilities
│   ├── animations.css          # Core @keyframes & 2D transform interactive classes
│   ├── components.css          # Navigation, hero, buttons, cards, toasts, loaders
│   └── responsive.css          # Mobile-first breakpoints & reduced-motion rules
│
├── assets/
│   └── images/
│       └── logo.svg            # Scalable vector brand emblem
│
├── .gitignore                  # Standard web gitignore
└── README.md                   # Project documentation
```

---

## CSS Architecture

The stylesheet architecture follows a modular, layer-oriented structure:

1. **`variables.css`**: Defines all fundamental design tokens in `:root` (colors, spacing, typography, radius, shadows, and easing curves). Also contains theme override classes (`.theme-emerald`, `.theme-cyber`, `.theme-sunset`, `.theme-midnight`).
2. **`base.css`**: Provides a modern CSS reset (`box-sizing: border-box`, margins, paddings), base typography hierarchy, layout containers (`.container`, `.section`), and accessible focus states.
3. **`animations.css`**: Declares reusable `@keyframes` animation definitions and transform test classes for GPU-accelerated motion.
4. **`components.css`**: Contains component patterns: header, hero, button variants, animated cards, 2D transform playground, keyframe gallery, status beacons, loaders, and pure CSS theme switcher logic.
5. **`responsive.css`**: Houses mobile-first layout rules progressive media queries (640px, 1024px, 1440px) and the `@media (prefers-reduced-motion: reduce)` accessibility overrides.
6. **`style.css`**: Serves as the master entrypoint, importing all layers in correct architectural cascade order.

---

## Design Tokens System

The design system relies on semantic custom properties declared in `:root`:

```css
:root {
  /* Color Tokens */
  --color-primary: #6366f1;
  --color-primary-hover: #4f46e5;
  --color-primary-glow: rgba(99, 102, 241, 0.35);
  --color-surface-card: #131c31;

  /* Spacing Scale */
  --space-xs: 0.5rem;   /* 8px */
  --space-md: 1rem;     /* 16px */
  --space-xl: 2rem;     /* 32px */

  /* Corner Radii */
  --radius-sm: 6px;
  --radius-md: 10px;
  --radius-pill: 9999px;

  /* Elevation Shadows */
  --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.45);
  --shadow-md: 0 4px 12px -2px rgba(0, 0, 0, 0.5);
  --shadow-xl: 0 24px 48px -12px rgba(0, 0, 0, 0.75);

  /* Motion Curves */
  --transition-fast: 150ms;
  --transition-normal: 250ms;
  --ease-standard: cubic-bezier(0.4, 0, 0.2, 1);
  --ease-spring: cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
```

---

## Motion & Animation System

Animations follow modern 60fps performance guidelines by strictly mutating composite-only properties: **`transform`** and **`opacity`**. Layout thrashing properties (such as animating `width`, `height`, `margin`, or `top`) are strictly avoided.

### Example: Spring Button Lift
```css
.btn {
  transition: 
    transform var(--transition-normal) var(--ease-standard),
    box-shadow var(--transition-normal) var(--ease-standard);
  will-change: transform, box-shadow;
}

.btn:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-md);
}

.btn:active {
  transform: translateY(0) scale(0.98);
}
```

---

## How to Run Locally

Because the project requires no compilation, bundler, or local server:

1. Clone or download the repository:
   ```bash
   git clone https://github.com/your-username/Animated-Ui-Theme-Pack.git
   ```
2. Navigate into the folder:
   ```bash
   cd Animated-Ui-Theme-Pack
   ```
3. Open `index.html` directly in your favorite browser (Chrome, Firefox, Safari, Edge):
   - Double-click `index.html` in your file explorer, OR
   - Run from terminal:
     ```bash
     # Windows PowerShell
     Start-Process index.html

     # macOS
     open index.html

     # Linux
     xdg-open index.html
     ```

---

## Accessibility & Reduced Motion

The theme pack is built with inclusive design principles:
- **Semantic Structure**: Proper landmark tags (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`) and appropriate heading levels (`<h1>` through `<h4>`).
- **Visible Keyboard Focus**: Interactive elements utilize high-contrast `:focus-visible` outlines offset from the component boundary.
- **Vestibular Sensitivity**: Respects user operating system settings for reduced motion:
  ```css
  @media (prefers-reduced-motion: reduce) {
    *, *::before, *::after {
      animation-duration: 0.01ms !important;
      animation-iteration-count: 1 !important;
      transition-duration: 0.01ms !important;
      scroll-behavior: auto !important;
    }
    .anim-float, .anim-pulse, .anim-spin, .anim-bounce {
      animation: none !important;
      transform: none !important;
    }
  }
  ```

---

## Browser Compatibility

Compatible with all modern web standards compliant browsers:
- Google Chrome & Chromium derivatives (Edge, Brave, Opera) &ge; 90
- Mozilla Firefox &ge; 88
- Apple Safari &ge; 14.1

---

## Future Enhancements

- [ ] Additional CSS-only theme presets (Monochrome Cyber, Forest Twilight).
- [ ] CSS Container Queries (`@container`) for granular sub-component responsiveness.
- [ ] Extended 3D perspective transform playground examples (`rotateX`, `rotateY`, `perspective`).
- [ ] Copy-to-clipboard CSS snippet utility integration.

---

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use and adapt these components in your own applications and design systems.
