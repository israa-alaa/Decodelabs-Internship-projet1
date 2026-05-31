# Decodelabs-Internship-projet1

# Israa — Crypto & AI Landing Page
 
A dark-themed, responsive landing page for a cryptocurrency and AI learning platform. Built with pure HTML and CSS, no frameworks required.
 
---
 
## Preview
 
The page features a deep space dark background, a sticky navigation header, a hero section with an animated side image, three topic cards (Bitcoin, Ethereum, AI), and a footer.
 
---
 
## Project Structure
 
```
project/
├── index.html      # Page markup and structure
├── landing.css     # All styles (layout, theme, components)
├── side-pic.png    # Hero section illustration (orbit/social graphic)
├── card1.png       # Bitcoin card image
├── card2.png       # Ethereum card image
└── card3.png       # AI card image
```
 
---
 
## Dependencies
 
No external libraries. One Google Fonts import is used via CDN.
 
| Resource | Type | Purpose |
|---|---|---|
| Jacques Francois | Google Font | Primary serif display font |
| Josefin Sans | Google Font | Imported (available for use) |
| Quicksand | Google Font | Imported (available for use) |
 
---
 
## How It Works
 
### Layout System
 
A `.container` class sets a centered, max-width layout at **1200px** with horizontal padding, used by every major section.
 
```css
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}
```
 
### Header
 
A flex row with `justify-content: space-between` distributes the logo, nav links, and login/signup buttons evenly at a fixed height of **80px**. Nav links highlight on hover with a purple underline transition.
 
### Hero Section (`.hero-container`)
 
A flex row with `justify-content: space-between` splits the page into two halves:
- **Left** — headline, subheadline, paragraph, and a Learn More button.
- **Right** — the `side-pic.png` illustration (orbit diagram with avatars and "20k+ Specialists").
### Cards Section
 
Three topic cards are laid out using **CSS Grid** with `auto-fit` and `minmax(278px, 288px)` columns, so they wrap naturally on smaller screens.
 
```css
grid-template-columns: repeat(auto-fit, minmax(278px, 288px));
gap: 24px;
justify-content: center;
```
 
Each card has:
- A full-width image (250px tall)
- A text area with a purple gradient background
- A hover effect that lifts the card upward by 10px
### Color Palette
 
| Role | Value |
|---|---|
| Page background | Gradient: `#04050c → #1a123a → #04050c` |
| Card background | `#120e26` |
| Card text area | Gradient: `#3b3266 → #262b53` |
| Borders & dividers | `#3b344c` |
| Accent / hover | `#53448c` |
| Footer background | `#0b0f19` |
 
### Footer
 
Fixed at **400px tall**, dark background (`#0b0f19`), centered copyright text. Separated from the main content by a top border.
 
---
 
## Transitions & Hover Effects
 
| Element | Effect |
|---|---|
| Nav links | Color changes to `#53448c`, underline appears — `ease-out 0.3s` |
| Login button | Bottom border appears |
| Sign Up button | Background fills to `#53448c` — `ease-in 0.3s` |
| Learn More button | Background clears, purple border appears |
| Cards | Lift up `translateY(-10px)`, border turns purple — `ease-out 0.3s` |
 
---
 
## Usage
 
1. Place all image files (`side-pic.png`, `card1.png`, `card2.png`, `card3.png`) in the same directory as `index.html`.
2. Open `index.html` in any modern browser — no build step needed.
3. To update content, edit the text directly in `index.html`.
4. To retheme, update the color values in `landing.css` (look for `#53448c` for the accent and `#04050c`/`#1a123a` for the background).
---
 
## Known Limitations
 
- No mobile/responsive breakpoints are defined — the layout is desktop-first and may overflow on narrow screens.
- The navbar has no hamburger menu for mobile.
- Card images use a fixed height of `250px`; differently sized source images may appear stretched.
- No JavaScript — buttons and nav links are not wired to any interaction beyond CSS hover states.
 
