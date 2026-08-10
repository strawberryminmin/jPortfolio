---
name: Luminous Kawaii OS
colors:
  surface: '#f4fafd'
  surface-dim: '#d4dbdd'
  surface-bright: '#f4fafd'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#eef5f7'
  surface-container: '#e8eff1'
  surface-container-high: '#e2e9ec'
  surface-container-highest: '#dde4e6'
  on-surface: '#161d1f'
  on-surface-variant: '#524248'
  inverse-surface: '#2b3234'
  inverse-on-surface: '#ebf2f4'
  outline: '#857279'
  outline-variant: '#d7c1c8'
  surface-tint: '#95416c'
  primary: '#95416c'
  on-primary: '#ffffff'
  primary-container: '#ff99c8'
  on-primary-container: '#7b2c56'
  inverse-primary: '#ffafd2'
  secondary: '#4f5f78'
  on-secondary: '#ffffff'
  secondary-container: '#d0e1ff'
  on-secondary-container: '#53637d'
  tertiary: '#636034'
  on-tertiary: '#ffffff'
  tertiary-container: '#c0bb86'
  on-tertiary-container: '#4e4b21'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#ffd8e6'
  primary-fixed-dim: '#ffafd2'
  on-primary-fixed: '#3d0025'
  on-primary-fixed-variant: '#782953'
  secondary-fixed: '#d4e3ff'
  secondary-fixed-dim: '#b7c7e5'
  on-secondary-fixed: '#0a1c32'
  on-secondary-fixed-variant: '#374860'
  tertiary-fixed: '#eae5ad'
  tertiary-fixed-dim: '#cec893'
  on-tertiary-fixed: '#1e1c00'
  on-tertiary-fixed-variant: '#4b481e'
  background: '#f4fafd'
  on-background: '#161d1f'
  surface-variant: '#dde4e6'
typography:
  display-expressive:
    fontFamily: Syne
    fontSize: 48px
    fontWeight: '800'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Bricolage Grotesque
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.2'
  headline-md:
    fontFamily: Bricolage Grotesque
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.5'
  label-sm:
    fontFamily: Plus Jakarta Sans
    fontSize: 12px
    fontWeight: '600'
    lineHeight: '1.2'
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  base: 8px
  window-padding: 24px
  desktop-margin: 32px
  gutter: 16px
  icon-grid: 80px
---

## Brand & Style

The design system evolves the "Electric OS" into a **Lofi/Kawaii OS** aesthetic, blending the nostalgia of a desktop environment with a modern, cozy, and playful sensibility. It targets creative professionals and developers who want to showcase personality through a digital "sanctuary."

The style is defined by **Glassmorphism** and **Soft Minimalism**. It features translucent, frosted window containers, rounded corners, and a pastel-heavy palette. Unlike the harsh lines of a traditional retro OS, this system uses high-quality blurs, organic shadows, and whimsical typography to create an interface that feels inviting, tactile, and emotionally resonant.

## Colors

The palette shifts from high-energy neon to a **Soft Pastel Foundation** with high-contrast accents. 

- **Primary (Bubblegum):** Used for window headers, active folder icons, and primary buttons.
- **Secondary (Soft Sky):** Used for selection states, dock backgrounds, and subtle gradients.
- **Tertiary (Primrose):** Used for "warning" states or decorative highlights to maintain the "Kawaii" warmth.
- **Neutral (Charcoal):** Reserved strictly for text and icon glyphs to ensure high legibility against pastel backgrounds.

The core of the interface relies on **Glass Surfaces**: semi-transparent white fills with a `20px` to `40px` backdrop blur, allowing the vibrant, illustrative wallpaper to bleed through softly.

## Typography

This design system uses a dual-font strategy to balance utility with whimsy. 

1.  **Functional Layer:** *Plus Jakarta Sans* provides a soft, rounded, and highly legible experience for body text, system labels, and navigation. 
2.  **Personality Layer:** *Bricolage Grotesque* is used for window titles and headers, offering a quirky, slightly irregular rhythm.
3.  **Expressive Layer:** *Syne* is utilized for hero moments (like the "Portfolio" text in the reference) to provide a bold, almost-handwritten artistic flair.

On mobile, `display-expressive` scales down to `32px` to ensure the "windowed" layout doesn't overflow horizontally.

## Layout & Spacing

The layout simulates a **Floating Desktop Environment**. 

- **Grid Model:** A 12-column fluid grid is used for content *within* windows, but the windows themselves are positioned on a flexible coordinate system.
- **Desktop Icons:** Placed on a strict `80px` grid on the left-hand side with `32px` margins from the screen edge.
- **Window Architecture:** Features a fixed-height top bar (`32px`) containing window controls (Close, Minimize, Maximize) styled as colorful "candy" dots.
- **Mobile Adaptation:** Windows transition to full-screen modals with a `16px` safe-area margin. The desktop dock transforms into a bottom-anchored navigation bar.

## Elevation & Depth

Hierarchy is established through **Backdrop Blur** and **Subtle Diffused Shadows**.

- **Level 1 (Desktop):** The base wallpaper layer.
- **Level 2 (Folders/Icons):** Flat icons with a subtle `2px` drop shadow to lift them from the background.
- **Level 3 (Windows):** The primary glass container. It uses a `1px` inner white border (50% opacity) to simulate a glass edge and a large, soft shadow (`0 20px 40px rgba(0,0,0,0.05)`).
- **Level 4 (Modals/Popovers):** Higher contrast glass with a secondary tint of the `primary_color` at 10% opacity to distinguish it from the main window.

## Shapes

The shape language is consistently **Rounded**. 

- **Windows:** Utilize `1.5rem` (24px) for the main container to emphasize the soft, modern feel.
- **Buttons & Inputs:** Use a pill-shaped `2rem` radius for a friendly, approachable touch.
- **Desktop Icons:** Use a soft `0.75rem` radius. 

Avoid sharp corners entirely to maintain the "Kawaii" and "Lofi" aesthetic.

## Components

### Window Containers
The signature component. It consists of a `primary-color` header bar with three circular control buttons (Red, Yellow, Green) on the left. The body is a glassmorphic surface with high backdrop blur.

### Folders & Icons
Illustrated, soft-colored icons. Folders should use a "squishy" appearance. When hovered, they should scale up slightly (1.05x) and show a subtle `secondary-color` glow.

### The Dock
A centered, floating bar at the bottom of the screen. It uses a more opaque glass effect than the windows. Icons within the dock should bounce or scale when hovered, mimicking classic OS behavior but with softer animations.

### Buttons
Primary buttons are solid `primary_color` with `neutral_color` text. Secondary buttons are "ghost" style with a `1px` border of the `primary_color` and a very subtle hover fill.

### Input Fields
Inputs should look like "carved" paths into the glass surface—semi-transparent with a soft inner shadow and a `plusJakartaSans` label floating above.