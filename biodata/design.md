# DESIGN.md — Bocchi-Inspired Cartoon Portfolio

## Project Goal

Polish the existing personal portfolio website into a **cartoon-style anime portfolio inspired by Bocchi the Rock**, while keeping the site readable, responsive, lightweight, and suitable for an academic assignment.

The final website should feel playful and expressive, but still organized enough to function as a real developer portfolio.

Do **not** rewrite the personal content unless necessary for layout or readability. Focus primarily on visual design, spacing, responsiveness, and presentation.

---

## Visual Direction

### Core Vibe

Use a visual style inspired by:

- Bocchi-style pink color palette
- Cute anime / cartoon UI
- Soft pastel surfaces
- Hand-drawn / sticker-like decorative elements
- Rounded cards
- Bold outlines
- Slightly exaggerated cartoon shadows
- Fun but controlled micro-interactions
- A playful developer portfolio rather than a formal corporate landing page

The website should feel like a mix of:

**anime profile page + cartoon UI + student developer portfolio**

Avoid making it look like:

- a corporate SaaS website
- a generic Bootstrap template
- an overly childish kids website
- a neon cyberpunk website
- a cluttered anime fan page

---

## Main Color Palette

Use these colors as the base palette.

```css
--bg-main: #fff7fb;
--bg-secondary: #ffeaf5;
--card: #ffffff;

--pink-primary: #f472b6;
--pink-strong: #ec4899;
--pink-soft: #fbcfe8;

--purple: #c084fc;
--purple-soft: #e9d5ff;

--yellow-accent: #fde68a;
--blue-accent: #93c5fd;

--text-main: #3f3f46;
--text-soft: #71717a;

--outline: #3f3f46;
```

The dominant colors should remain **pink + white + soft purple**.

Use yellow and blue only as secondary accents.

---

## Cartoon Styling Rules

Use a consistent cartoon treatment across components.

### Cards

Cards should have:

- rounded corners
- visible dark outline
- light pastel background
- simple offset shadow
- slightly playful appearance

Example direction:

```css
border: 2px solid #3f3f46;
border-radius: 20px;
box-shadow: 6px 6px 0 #3f3f46;
```

Hover interaction:

```css
transform: translate(-2px, -2px);
box-shadow: 9px 9px 0 #3f3f46;
```

Do not use heavy glassmorphism.

---

## Typography

Prefer friendly, rounded-looking typography.

If external fonts are allowed, use:

- **Poppins** for body text
- **Fredoka** or **Nunito** for headings

If avoiding external fonts, use:

```css
font-family: "Trebuchet MS", Arial, sans-serif;
```

Headings should feel expressive but remain readable.

Do not use overly decorative fonts for paragraphs.

---

## Hero Section

The hero section should be the strongest visual area of the page.

### Layout

Desktop:

```text
+-------------------------------------------------------+
|                                                       |
|  Intro Text                          Character Art     |
|  Hallo, ich heiße Rayyan             Bocchi image     |
|  short description                                    |
|  tags / buttons                                       |
|                                                       |
+-------------------------------------------------------+
```

Mobile:

```text
Intro
Description
Buttons / Tags
Character illustration
```

### Hero Content

Keep the existing introduction.

Add optional small badges such as:

- Informatics Student
- Web Development
- AI
- Data Science

Badges should look like cartoon stickers.

### Character Illustration

Use the existing/local Bocchi-themed image if available.

Do not fetch or hotlink random copyrighted images automatically.

If no character image exists, keep the layout ready for:

```html
assets/bocchi.png
```

The character should sit naturally in the hero instead of appearing like a random rectangular image.

Possible styling:

- transparent PNG
- no hard rectangular background
- subtle floating animation
- small decorative doodles around it

Do not make the character image cover important text.

---

## Decorative Elements

Add small cartoon decorations around the layout.

Examples:

- stars
- music notes
- tiny hearts
- sparkles
- simple circles
- scribble lines
- guitar / music motifs
- small coding symbols such as `</>`

Prefer CSS shapes or simple Unicode characters.

Keep decoration subtle.

Decorations should never reduce readability.

---

## Navbar

Add a sticky or top navigation bar.

Suggested links:

- About
- Skills
- Projects
- Education
- GitHub
- Contact

Style:

- white/pink card-like navbar
- rounded container
- cartoon outline
- responsive menu on small screens

Do not make the navbar excessively tall.

---

## About / Profile Section

Present profile information in a more visual layout.

Instead of plain paragraphs only, consider:

```text
Name            Rayyan
Nickname        Rayyan
NIM             2024520047
Study Program   Informatika
Location        Pamekasan, Jawa Timur
```

Possible presentation:

- mini profile cards
- two-column info grid
- label/value layout

Keep semantic HTML.

---

## Motivation Section

Make this section resemble a quote card or dialogue panel.

Visual idea:

- pastel purple / pink background
- speech-bubble feeling
- quotation marks
- small decorative icon

Do not change the meaning of the existing motivation text.

---

## Tech Stack Section

Replace the plain table visually if possible, while keeping the information intact.

Preferred presentation:

### Desktop

A responsive grid of skill cards:

```text
Python          Basic
PHP             Basic
Next.js         Learning
Flutter         Learning
...
```

Each skill can be shown as:

```text
[ icon/name ]
[ level badge ]
```

If icons are used, prefer lightweight solutions.

Do not add fake proficiency percentages such as:

```text
Python 85%
```

unless already provided by the user.

Use only the stated levels:

- Basic
- Sedang Dipelajari

---

## Project Section

This should be one of the best-looking sections.

Display projects as responsive cards.

Each project card should include:

- project title
- short description
- tech stack
- source code button

Projects currently include:

- MyTools
- Drink Cashier
- MySavings
- Face Detection
- Docx2PDF
- Background Remover

### Card Style

Use a two-column grid on larger screens.

Use one column on mobile.

Each card should have:

- cartoon outline
- pastel accent
- hover animation
- consistent button placement

Possible small accent colors can vary slightly per card while staying inside the main palette.

Do not remove or modify the GitHub URLs.

---

## Education Section

Use a vertical timeline or connected cards.

Example:

```text
2024 — Present
Universitas Madura
Informatika

2021 — 2024
MA Mambaul Ulum 1 Bata-Bata
```

Use simple cartoon nodes and connecting lines.

Keep it responsive.

---

## GitHub Activity Section

Make GitHub activity visually distinct.

Show:

- GitHub profile link
- repository activity description
- commit history link if available
- minimum 3 commit evidence

Possible UI:

```text
● Commit 1 — Initial project structure
● Commit 2 — Add personal biodata and portfolio content
● Commit 3 — Add anime-themed responsive styling
```

Do not fabricate commits that do not exist yet.

If commit #3 has not been made, leave the structure ready and only show existing commits.

---

## Video Praktikum Section

Create a card ready for the future video URL.

Current placeholder `href="#"` may remain until the real URL exists.

Style the button as a prominent CTA:

```text
▶ Tonton Video Praktikum
```

Do not invent a video URL.

---

## Contact Section

Only show contact links already approved by the user.

Current safe contact options:

- GitHub
- Instagram
- TikTok

Do not add:

- phone number
- WhatsApp number
- private email
- API keys
- Telegram bot tokens
- other sensitive information

---

## Buttons

Use consistent cartoon buttons.

Example:

```css
.button {
    display: inline-block;
    padding: 10px 18px;
    background: #f472b6;
    color: white;
    border: 2px solid #3f3f46;
    border-radius: 14px;
    box-shadow: 4px 4px 0 #3f3f46;
    transition: 0.2s ease;
}

.button:hover {
    transform: translate(-2px, -2px);
    box-shadow: 6px 6px 0 #3f3f46;
}
```

Use buttons for:

- Source Code
- GitHub
- Video Praktikum
- important navigation actions

---

## Animations

Animations should be subtle.

Allowed examples:

- character floating slowly
- cards slightly lifting on hover
- decorative stars moving slightly
- buttons bouncing a few pixels
- fade-in when page loads

Avoid:

- constant shaking
- flashing
- rapid animation
- huge parallax effects
- excessive JavaScript animation

Respect:

```css
@media (prefers-reduced-motion: reduce)
```

and disable unnecessary animations for users who prefer reduced motion.

---

## Responsive Behavior

The website must look good at:

### Desktop
- 1440px
- 1366px
- 1024px

### Tablet
- around 768px

### Mobile
- around 375px
- around 430px

Rules:

- hero changes from 2 columns to 1
- project grid changes to 1 column
- skills grid adjusts automatically
- navigation should not overflow
- text should stay readable
- images should use `max-width: 100%`
- no horizontal scrolling

---

## Accessibility

Maintain:

- sufficient color contrast
- semantic heading hierarchy
- alt text for meaningful images
- visible keyboard focus states
- readable font sizes
- buttons/links large enough to tap on mobile

Do not rely only on color to communicate meaning.

---

## Code Quality

Keep the implementation simple and understandable for a student project.

Prefer:

```text
index.html
style.css
assets/
```

Do not unnecessarily introduce:

- React
- Tailwind
- Bootstrap
- large JavaScript frameworks
- build tools

unless the existing project already uses them.

Use clean CSS sections with comments.

Example:

```css
/* =========================
   HERO
   ========================= */
```

---

## Important Content Rules

The existing text represents the student's actual profile.

Therefore:

1. Do not invent new skills.
2. Do not increase skill levels.
3. Do not invent projects.
4. Do not remove project links.
5. Do not invent education history.
6. Do not change NIM.
7. Do not replace personal text with generic AI copy.
8. Do not add private contact information.
9. Do not remove the required academic content.
10. Preserve the user's personality.

Small grammar and spacing improvements are allowed.

---

## Copyright / Character Art

The design may be **inspired by Bocchi the Rock**, but the code should not automatically download official character artwork from the internet.

Use a locally provided image if the user supplies one.

Expected optional asset:

```text
biodata/assets/bocchi.png
```

The rest of the design should still work if the image is temporarily unavailable.

---

## Desired Final Impression

When someone opens the page, the desired reaction is:

> "This is clearly a student developer portfolio, but it has a very personal anime/cartoon identity."

It should be:

- cute
- distinctive
- slightly chaotic in a controlled way
- pink
- cartoon-like
- anime-inspired
- readable
- responsive
- still suitable for university assessment

---

## Implementation Priority

Work in this order:

1. Fix page layout and spacing.
2. Add the color system.
3. Create hero layout.
4. Create navbar.
5. Restyle profile and motivation.
6. Convert tech stack into responsive cards.
7. Create polished project cards.
8. Create education timeline.
9. Style GitHub / video / contact sections.
10. Add subtle decorations.
11. Add responsive rules.
12. Add subtle animations.
13. Test mobile and desktop layouts.
14. Verify that no content or links were accidentally removed.

---

## Final Constraint

Do not over-engineer the page.

The goal is a polished **HTML + CSS student portfolio**, not a production application.

The visual identity matters, but clarity and responsiveness matter more.
