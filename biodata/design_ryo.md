# DESIGN.md — Ryo Yamada-Inspired Cartoon Portfolio

## Project Goal

Polish the existing personal portfolio website into a **cartoon-style anime portfolio inspired by Ryo Yamada from Bocchi the Rock**, while keeping the site readable, responsive, lightweight, and suitable for an academic assignment.

The final website should feel cool, quirky, dry-humored, and visually distinct — like a student developer portfolio with a calm anime bassist aesthetic.

Do **not** rewrite the personal content unless necessary for layout or readability. Focus primarily on visual design, spacing, responsiveness, and presentation.

---

## Visual Direction

### Core Vibe

Use a style inspired by:

- cool blue / teal palette
- calm anime bassist energy
- minimalist cartoon UI
- slightly deadpan / quirky personality
- soft rounded panels
- bold cartoon outlines
- offset shadows
- music-inspired decorations
- clean developer portfolio structure

The website should feel like:

**anime bassist profile + cartoon UI + student developer portfolio**

Avoid making it look like:

- a corporate SaaS landing page
- generic Bootstrap
- cyberpunk neon
- overly cute pink kawaii UI
- dark hacker terminal
- cluttered anime fan site

---

## Main Color Palette

Use this palette as the main visual system.

```css
--bg-main: #eef7fb;
--bg-secondary: #dff3f7;
--card: #ffffff;

--blue-primary: #4f86c6;
--blue-strong: #2f5f8f;
--blue-soft: #bcdff1;

--teal-primary: #5bc0be;
--teal-soft: #c9f1ee;

--navy: #243447;
--navy-soft: #3b556d;

--yellow-accent: #f5d76e;
--green-accent: #94c973;

--text-main: #263238;
--text-soft: #607d8b;

--outline: #263238;
```

Dominant colors:

- muted blue
- teal
- white
- desaturated navy

Use yellow or green only as small accents.

---

## Overall Art Direction

The design should be cartoon-like, but not childish.

Think:

- clean comic panel shapes
- rounded cards
- thick outlines
- simple shadows
- subtle hand-drawn feel
- understated anime personality

The page should feel more "cool and weird" than "cute and bubbly".

---

## Cartoon Styling Rules

### Cards

Use:

```css
border: 2px solid #263238;
border-radius: 18px;
box-shadow: 6px 6px 0 #263238;
```

Hover:

```css
transform: translate(-2px, -2px);
box-shadow: 9px 9px 0 #263238;
```

Cards may use different pale blue/teal backgrounds.

Avoid:

- glassmorphism
- glowing neon borders
- excessive gradients
- heavy blur

---

## Typography

Prefer simple, slightly rounded fonts.

If external fonts are allowed:

- **Nunito**
- **Poppins**
- **Fredoka** for small expressive headings only

Fallback:

```css
font-family: "Trebuchet MS", Arial, sans-serif;
```

Headings may be bold and slightly oversized.

Body text should remain simple and readable.

---

## Hero Section

The hero section should immediately communicate the theme.

### Desktop Layout

```text
+------------------------------------------------------+
|                                                      |
|  Intro Text                        Ryo Illustration   |
|  Hallo, ich heiße Rayyan           Character Art     |
|  short developer description                         |
|  tags / CTA buttons                                  |
|                                                      |
+------------------------------------------------------+
```

### Mobile Layout

```text
Intro
Description
Tags / Buttons
Character Illustration
```

### Hero Style

Use:

- pale blue background
- large rounded shapes
- small bass-guitar/music decorations
- subtle teal accents
- slightly oversized cartoon title
- character illustration placed naturally on the side

---

## Character Illustration

Use a locally provided Ryo-themed image if available.

Expected asset:

```text
biodata/assets/ryo.png
```

Do not automatically download official anime artwork.

The image should ideally be:

- transparent PNG
- character cutout
- not inside a hard rectangular frame
- placed as part of the composition

Optional effect:

```css
animation: float 4s ease-in-out infinite;
```

Keep animation subtle.

---

## Decorative Elements

Use small decorations related to:

- bass guitar
- music notes
- stars
- leaves / plants
- small scribbles
- brackets
- code symbols
- simple geometric shapes

Examples:

```text
♪  ♫  ✦  </>  { }  ●
```

Decorations should be sparse.

Ryo-inspired theme should feel controlled and understated.

---

## Navbar

Add a simple floating/sticky navbar.

Suggested links:

- About
- Skills
- Projects
- Education
- GitHub
- Contact

Style:

- white or pale blue card
- navy outline
- rounded shape
- offset cartoon shadow
- compact spacing

On mobile, avoid overflow.

---

## About / Profile Section

Display profile details as compact info cards or a grid.

Example:

```text
Name            Rayyan
Nickname        Rayyan
NIM             2024520047
Study Program   Informatika
Location        Pamekasan, Jawa Timur
```

Possible look:

- label on left
- value on right
- alternating pale blue / teal strips
- simple icon or dot

Keep it clean.

---

## Motivation Section

Make the motivation section feel like a comic dialogue or thought panel.

Use:

- light teal / blue background
- rounded speech-bubble-like card
- small quotation mark
- subtle icon

Do not change the meaning of the original motivation text.

---

## Tech Stack Section

Avoid plain tables if possible.

Convert skills into responsive cards.

Example:

```text
Python
Basic

Next.js
Sedang Dipelajari

Flutter
Sedang Dipelajari
```

Card styling:

- pale blue background
- dark outline
- small level badge
- 2–4 columns depending on viewport

Do not invent percentages.

Do not upgrade skill levels.

Use only the user's current labels:

- Basic
- Sedang Dipelajari

---

## Project Section

Use a card grid.

Current projects:

- MyTools
- Drink Cashier
- MySavings
- Face Detection
- Docx2PDF
- Background Remover

Each card should include:

- project title
- short description
- tech stack
- source code button

### Visual Style

Cards should feel like small comic panels.

Possible accent variations:

- blue
- teal
- navy
- muted green

Keep accents consistent with the overall palette.

Do not remove or modify GitHub project URLs.

---

## Education Section

Use a vertical timeline.

Example:

```text
2024 — Present
Universitas Madura
Informatika

2021 — 2024
MA Mambaul Ulum 1 Bata-Bata
```

Style:

- navy line
- teal/blue circular timeline markers
- small cartoon labels
- readable spacing

Avoid overcomplicated timeline animations.

---

## GitHub Activity Section

Make it visually distinct.

Show:

- GitHub profile link
- description of repository development
- commit history link
- commit evidence

Possible layout:

```text
● Initial project structure
● Add personal biodata and portfolio content
● Add Ryo-themed responsive styling
```

Do not fabricate commits that do not exist yet.

If the current styling commit has not been made, leave the UI ready and only show existing commits.

---

## Video Praktikum Section

Style this as a highlighted action panel.

Suggested button:

```text
▶ Tonton Video Praktikum
```

Use a stronger blue or teal background.

The current placeholder may remain until the actual video URL exists.

Do not invent URLs.

---

## Contact Section

Only keep safe, approved public links.

Current contact options:

- GitHub
- Instagram
- TikTok

Do not add:

- phone number
- WhatsApp
- private email
- Telegram bot tokens
- API keys
- personal secrets

---

## Buttons

Use consistent cartoon buttons.

Example:

```css
.button {
    display: inline-block;
    padding: 10px 18px;
    background: #5bc0be;
    color: #263238;
    border: 2px solid #263238;
    border-radius: 12px;
    box-shadow: 4px 4px 0 #263238;
    font-weight: 700;
    transition: 0.2s ease;
}

.button:hover {
    transform: translate(-2px, -2px);
    box-shadow: 6px 6px 0 #263238;
}
```

Use buttons for:

- Source Code
- GitHub
- Video Praktikum
- key navigation actions

---

## Optional Personality Details

The page may include subtle Ryo-like quirks without becoming a meme page.

Examples:

- tiny bassist/music note near headings
- small plant doodles
- dry microcopy in decorative labels
- tiny badge like `bassist-mode`
- one or two quirky visual callouts

Do not rewrite the user's actual profile text into jokes.

Keep humor purely decorative.

---

## Animations

Allowed:

- gentle floating character
- card lift on hover
- tiny music note movement
- button bounce by a few pixels
- fade-in on load

Avoid:

- flashing
- shaking
- strong parallax
- rapid motion
- distracting looping animations

Respect:

```css
@media (prefers-reduced-motion: reduce)
```

Disable non-essential animations in reduced-motion mode.

---

## Responsive Behavior

Target:

### Desktop
- 1440px
- 1366px
- 1024px

### Tablet
- 768px

### Mobile
- 375px
- 430px

Rules:

- hero becomes single-column on mobile
- project grid becomes 1 column
- skills grid reduces columns automatically
- navbar must not overflow
- character art scales down
- no horizontal scrolling
- text stays readable
- buttons remain tappable

---

## Accessibility

Maintain:

- semantic heading hierarchy
- meaningful alt text
- sufficient text contrast
- visible keyboard focus
- readable font sizes
- adequate button sizes
- no meaning conveyed by color alone

---

## Code Quality

Keep implementation understandable for a student.

Preferred structure:

```text
index.html
style.css
assets/
```

Do not introduce unnecessary:

- React
- Tailwind
- Bootstrap
- JS frameworks
- build tools

unless already used by the project.

Organize CSS with comments.

Example:

```css
/* =========================
   PROJECT CARDS
   ========================= */
```

---

## Important Content Rules

The current portfolio content is the user's real profile.

Therefore:

1. Do not invent skills.
2. Do not increase skill levels.
3. Do not invent projects.
4. Do not delete project URLs.
5. Do not invent education history.
6. Do not modify the NIM.
7. Do not replace content with generic AI copy.
8. Do not add private contact information.
9. Preserve all required assignment content.
10. Preserve the user's tone and personality.

Small grammar and spacing improvements are allowed.

---

## Copyright / Character Art

The design may be **inspired by Ryo Yamada / Bocchi the Rock**, but the implementation must not automatically download official copyrighted artwork.

Use a local image supplied by the user.

Expected asset:

```text
biodata/assets/ryo.png
```

The layout should still work even if the image is temporarily missing.

---

## Desired Final Impression

The desired reaction should be:

> "This looks like a cool anime bassist-themed developer portfolio, not a generic template."

It should feel:

- calm
- quirky
- cool
- blue/teal
- cartoon-like
- anime-inspired
- slightly deadpan
- clean
- readable
- responsive
- still appropriate for university assessment

---

## Implementation Priority

Work in this order:

1. Fix layout and spacing.
2. Apply blue / teal palette.
3. Build the hero composition.
4. Add navbar.
5. Restyle profile and motivation.
6. Convert tech stack into cards.
7. Build project card grid.
8. Create education timeline.
9. Style GitHub / video / contact.
10. Add subtle music and cartoon decorations.
11. Add responsive rules.
12. Add subtle animations.
13. Test desktop and mobile.
14. Verify all content and links remain intact.

---

## Final Constraint

Do not over-engineer the website.

The target is a polished **HTML + CSS student portfolio with a Ryo-inspired cartoon visual identity**, not a production web application.
