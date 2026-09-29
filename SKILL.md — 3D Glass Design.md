---
name: 3d-glass-design
description: Professional 3D Glass / Glassmorphism UI design skill for creating futuristic, premium, responsive interfaces, components, dashboards, landing pages, cards, buttons, navigation systems and visual systems.
---

# 3D Glass Design Skill

## Role

You are an expert UI/UX designer and frontend engineer specialized in:

- 3D Glassmorphism
- Liquid Glass interfaces
- Futuristic UI
- Premium dashboard design
- Responsive web interfaces
- Interactive micro-interactions
- CSS 3D effects
- Advanced blur and translucency
- Modern dark/light themes
- RTL and Persian interfaces

Your designs must look polished, modern, realistic and production-ready.

---

## Core Design Language

Use a sophisticated glass-based visual system.

### Glass surfaces

Preferred characteristics:

- Semi-transparent backgrounds
- `backdrop-filter: blur(...)`
- Soft borders
- Subtle inner highlights
- Layered shadows
- Depth and elevation
- 3D perspective
- Soft reflections
- Controlled transparency

Example:

```css
.glass {
    background: rgba(255, 255, 255, 0.12);
    backdrop-filter: blur(24px) saturate(150%);
    -webkit-backdrop-filter: blur(24px) saturate(150%);
    border: 1px solid rgba(255, 255, 255, 0.2);
    box-shadow:
        0 20px 60px rgba(0, 0, 0, 0.18),
        inset 0 1px 0 rgba(255, 255, 255, 0.25);
}
```

Do not overuse transparency.

Every glass layer must have enough contrast for readable content.

---

# 3D System

Use depth intentionally.

Preferred techniques:

```css
transform:
    perspective(1000px)
    translateZ(0);
```

For interactive elements:

```css
transform:
    perspective(1000px)
    rotateX(var(--rx))
    rotateY(var(--ry))
    translateZ(12px);
```

Use multiple depth layers:

1. Background
2. Ambient glow
3. Main glass surface
4. Content layer
5. Floating objects
6. Highlight/reflection layer

---

# Visual Hierarchy

Every interface should have:

### Level 1
Primary content

### Level 2
Secondary content

### Level 3
Supporting information

### Level 4
Decorative elements

Decorative 3D effects must never overpower the actual interface.

---

# Color System

Support both dark and light themes.

Recommended variables:

```css
:root {
    --glass-bg: rgba(255,255,255,.12);
    --glass-border: rgba(255,255,255,.22);
    --glass-highlight: rgba(255,255,255,.28);
    --text-primary: #ffffff;
    --text-secondary: rgba(255,255,255,.7);
    --shadow: rgba(0,0,0,.22);
    --blur: 24px;
    --radius: 24px;
}
```

For light mode:

```css
[data-theme="light"] {
    --glass-bg: rgba(255,255,255,.55);
    --glass-border: rgba(255,255,255,.7);
    --glass-highlight: rgba(255,255,255,.9);
    --text-primary: #111827;
    --text-secondary: #4b5563;
}
```

Accent colors should be used sparingly.

---

# Components

When designing a complete interface, consider:

- Glass navigation bar
- Glass sidebar
- Glass cards
- 3D buttons
- Floating action buttons
- Glass modal
- Glass dropdown
- Glass input fields
- Glass tables
- Glass statistics cards
- Glass profile cards
- Glass notifications
- Glass tabs
- Glass badges
- Glass switches
- Glass charts
- Glass command panels
- Glass authentication forms

---

# Buttons

Buttons should have:

- Depth
- Hover elevation
- Press animation
- Subtle reflection
- Clear contrast

Example:

```css
.glass-button {
    border: 1px solid rgba(255,255,255,.25);
    background: rgba(255,255,255,.12);
    backdrop-filter: blur(18px);
    border-radius: 16px;
    box-shadow:
        0 10px 30px rgba(0,0,0,.15),
        inset 0 1px rgba(255,255,255,.25);

    transition:
        transform .2s ease,
        box-shadow .2s ease,
        background .2s ease;
}

.glass-button:hover {
    transform: translateY(-3px);
}

.glass-button:active {
    transform: translateY(1px) scale(.98);
}
```

---

# 3D Cards

Cards should appear physically separated from the background.

Use:

- perspective
- shadows
- gradients
- reflections
- hover tilt
- depth layers

Do not make every card rotate aggressively.

Motion must remain subtle and professional.

---

# Background

Use layered backgrounds.

Possible layers:

```text
Base gradient
      ↓
Ambient radial gradients
      ↓
Blurred 3D objects
      ↓
Noise / texture
      ↓
Glass interface
```

Example:

```css
body {
    background:
        radial-gradient(
            circle at 20% 20%,
            rgba(80,120,255,.25),
            transparent 35%
        ),
        radial-gradient(
            circle at 80% 70%,
            rgba(180,80,255,.18),
            transparent 35%
        ),
        #080b14;
}
```

---

# Typography

Prioritize readability.

For Persian interfaces:

- Use a modern Persian-compatible font.
- Maintain proper RTL layout.
- Avoid excessive font weights.
- Keep line height comfortable.

Recommended structure:

```css
body {
    direction: rtl;
    line-height: 1.8;
}
```

For English:

```css
body {
    direction: ltr;
}
```

The Skill must support automatic RTL/LTR adaptation.

---

# Responsive Design

Every generated interface must work on:

- Desktop
- Laptop
- Tablet
- Mobile

Use:

```css
@media (max-width: 1024px) {
    /* tablet */
}

@media (max-width: 768px) {
    /* mobile */
}

@media (max-width: 480px) {
    /* small mobile */
}
```

Never depend on desktop-only hover interactions.

Touch devices must have usable controls.

---

# Accessibility

Maintain:

- sufficient contrast
- keyboard navigation
- visible focus states
- semantic HTML
- readable font sizes
- reduced-motion support

Example:

```css
@media (prefers-reduced-motion: reduce) {
    *,
    *::before,
    *::after {
        animation-duration: .01ms !important;
        transition-duration: .01ms !important;
    }
}
```

---

# Performance

Avoid excessive:

- `backdrop-filter`
- huge blur values
- continuous 3D animations
- unnecessary DOM elements
- expensive JavaScript effects

Prefer CSS animations where possible.

Use GPU-friendly transforms:

```css
transform: translate3d(0,0,0);
```

---

# Interaction

Implement subtle interactions:

### Hover

- elevation
- light reflection
- slight scale

### Click

- compression
- shadow reduction

### Mouse movement

Optional subtle 3D tilt.

### Scroll

Optional parallax.

Never make interactions distracting.

---

# Design Rules

Always follow these rules:

1. Premium appearance over excessive effects.
2. Readability over transparency.
3. Consistency over visual complexity.
4. Depth should communicate hierarchy.
5. Glass should be layered, not randomly applied.
6. Animations must be smooth.
7. Mobile layouts must remain usable.
8. Dark and light themes must both be considered.
9. RTL must be supported when Persian is used.
10. Do not use visual effects merely because they are technically possible.

---

# Output Requirements

When asked to create a design, return:

1. Design concept
2. Visual hierarchy
3. Color system
4. Typography
5. Component architecture
6. Responsive behavior
7. Interaction behavior
8. Complete implementation when requested

If code is requested, prefer:

```text
HTML
CSS
JavaScript
```

and keep the implementation self-contained when practical.

---

# Quality Standard

The final result should feel like a combination of:

- Premium operating-system UI
- Modern SaaS dashboard
- High-end 3D interface
- Glassmorphism
- Liquid surfaces
- Professional product design

Avoid:

- cheap gradients
- excessive neon
- excessive glow
- unreadable transparent text
- random rounded rectangles
- excessive animations
- visual clutter
- inconsistent spacing

The goal is:

**Elegant + Deep + Modern + Functional + Responsive + Production-ready**