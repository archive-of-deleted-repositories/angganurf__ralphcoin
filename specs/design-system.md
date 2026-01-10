# $RALPH Design System

## Color Palette

### Primary Colors (Simpsons-Inspired)

| Name | Hex | Usage |
|------|-----|-------|
| Simpsons Yellow | `#FFD90F` | Primary brand color, headings, CTAs, highlights |
| Simpsons Yellow Dark | `#E5C200` | Hover states, secondary accents |
| Simpsons Orange | `#FF6B00` | Gradients, accents, timeline markers |
| Simpsons Blue | `#00AAFF` | Secondary accent, intro text, aspirations |
| Simpsons Blue Dark | `#0088CC` | Hover states for blue elements |
| Simpsons Pink | `#FF69B4` | Future/roadmap indicators |
| Simpsons Sky | `#87CEEB` | Background gradients |

### Neutral Colors

| Name | Hex | Usage |
|------|-----|-------|
| White | `#FFFFFF` | Text highlights, logo shadows |
| Dark | `#1a1a2e` | Backgrounds, buttons, contrast elements |
| Darker | `#0f0f1a` | Deep backgrounds, footer |
| Text Light | `#f5f5f5` | Body text on dark backgrounds |
| Text Dark | `#333333` | Text on light/yellow backgrounds |

## Typography

### Font Families

| Font | Usage |
|------|-------|
| **Bangers** | Headings (h1-h4), logo, buttons, milestone dates, stats |
| **Comic Neue** | Body text, paragraphs, descriptions |
| **Fira Code / Courier New** | Code blocks, terminal commands, footer tagline |

### Font Sizes

| Element | Size | Notes |
|---------|------|-------|
| Hero H1 | 5rem (3rem mobile) | With text-shadow animation |
| Section H2 | 3rem (2.2rem mobile) | Yellow with orange shadow |
| Card H3 | 1.3-1.5rem | Yellow color |
| Body Text | 1.1rem | Line-height 1.8 |
| Small Text | 0.85-0.95rem | Disclaimers, subtitles |
| Code | 1.3rem (0.9rem mobile) | Monospace |

### Text Shadows

```css
/* Hero title */
text-shadow: 4px 4px 0 var(--simpsons-orange), 8px 8px 0 var(--dark);

/* Section headings */
text-shadow: 3px 3px 0 var(--simpsons-orange);

/* Logo */
text-shadow: 3px 3px 0 var(--white), -1px -1px 0 var(--white);
```

## Spacing

| Size | Value | Usage |
|------|-------|-------|
| Section padding | 100px 0 | Vertical section spacing |
| Container max-width | 1200px | Content constraint |
| Card padding | 25-35px | Internal card spacing |
| Grid gap | 30px | Between cards/items |
| Button padding | 15px 40px | Standard buttons |
| Button padding (large) | 20px 60px | CTA buttons |

## Components

### Buttons

#### Primary Button
- Background: Yellow to orange gradient
- Color: Dark text
- Border-radius: 50px
- Shadow: Yellow glow
- Hover: Scale 1.05, lift -3px

#### Secondary Button
- Background: Transparent
- Border: 3px solid yellow
- Color: Yellow
- Hover: Fill yellow, dark text

#### Dark Button
- Background: Dark
- Color: Yellow
- Shadow: Dark glow
- Used on light/yellow backgrounds

### Cards

#### Standard Card
```css
background: rgba(255, 255, 255, 0.05);
border-radius: 20px;
padding: 35px;
border: 2px solid transparent;
transition: all 0.3s ease;
```

Hover state:
```css
border-color: var(--simpsons-yellow);
transform: translateY(-10px);
background: rgba(255, 217, 15, 0.1);
```

#### Quote Box
- Gradient background (yellow → orange)
- Slight rotation: -1deg
- Box shadow: 5px 5px 0 dark
- Dark text on light background

### Code Block

```css
.code-block {
    border-radius: 15px;
    overflow: hidden;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.5);
}

.code-header {
    background: #2d2d2d;
    /* macOS-style dots: red, yellow, green */
}

.code-block pre {
    background: #1a1a1a;
    padding: 30px;
}
```

### Timeline

- Vertical line: Yellow to orange gradient, 4px wide
- Nodes: 24px circles, yellow with dark border
- Alternating left/right layout
- Responsive: Single column on mobile

### Milestone Cards

Status indicators via top border gradient:
- **Completed**: Green gradient
- **In Progress**: Yellow/orange gradient
- **Upcoming**: Blue gradient
- **Future**: Pink gradient

## Animations

### Bounce (Hero)
```css
@keyframes bounce {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-10px); }
}
```

### Wiggle (Logo hover)
```css
@keyframes wiggle {
    0%, 100% { transform: rotate(0deg); }
    25% { transform: rotate(3deg); }
    75% { transform: rotate(-3deg); }
}
```

### Standard Transitions
- Duration: 0.3s
- Easing: ease
- Properties: transform, background, border-color, box-shadow

## Responsive Breakpoints

| Breakpoint | Changes |
|------------|---------|
| 968px | Timeline single column, stat cards wrap |
| 768px | Nav hidden, hero text smaller, single column grids, stacked social cards |

## Gradients

### Primary Gradient
```css
linear-gradient(135deg, var(--simpsons-yellow) 0%, var(--simpsons-orange) 100%)
```

### Background Gradient
```css
linear-gradient(180deg, var(--dark) 0%, var(--darker) 100%)
```

### Hero Sky Effect
```css
radial-gradient(ellipse at top, var(--simpsons-sky) 0%, transparent 50%)
```

## Links

### On Dark Backgrounds
- Color: Yellow
- Border-bottom: 2px solid orange
- Hover: Orange text, yellow border

### On Light/Yellow Backgrounds
- Color: Dark
- Font-weight: 700
- Border-bottom: 1px solid dark
- Hover: Reduced opacity

## Scrollbar (WebKit)

```css
::-webkit-scrollbar { width: 10px; }
::-webkit-scrollbar-track { background: var(--darker); }
::-webkit-scrollbar-thumb { background: var(--simpsons-yellow); border-radius: 5px; }
::-webkit-scrollbar-thumb:hover { background: var(--simpsons-orange); }
```
