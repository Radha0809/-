# Shreyu Birthday Website — Design Brainstorm

## Teen Possible Directions

### Theme Name: Burgundy Botanical Editorial
Very Brief Intro: Ek soft, editorial birthday experience jisme ivory paper, deep burgundy typography aur orchid photography ka refined mix hoga. Mood intimate, poetic aur premium rahega.
Probability: 0.07

### Theme Name: Champagne Keepsake Album
Very Brief Intro: Warm champagne tones, scrapbook-inspired photo frames aur handwritten accents ke saath ek nostalgic memory-book feel. Mood cozy, personal aur celebratory rahega.
Probability: 0.04

### Theme Name: Midnight Dawn Letter
Very Brief Intro: Deep ink background, moonlit florals aur warm dawn highlights ke saath ek cinematic digital letter. Mood dramatic, hopeful aur emotionally powerful rahega.
Probability: 0.06

## Selected Direction: Burgundy Botanical Editorial

### Design Movement
Contemporary editorial romanticism, inspired by luxury stationery, botanical still-life photography, and quiet magazine layouts. The design will feel composed rather than overly decorative.

### Core Principles
1. Typography is the primary emotional layer: large Baskerville-style lines for feeling, Gilroy/Helvetica Neue for clarity.
2. Burgundy is used as a deliberate ink colour, not a loud accent; ivory space gives the message room to breathe.
3. Photography feels tactile and framed, like keepsakes placed on a gallery table rather than generic cards.
4. Motion stays soft and physical: blur, opacity, and horizontal drift should feel like turning pages.

### Color Philosophy
The foundation is #F5F1EB, a warm paper ivory that keeps the page gentle and luminous. #FFFFFF is reserved for breathing spaces and elevated photo surfaces. #CDB49E adds a muted champagne-beige warmth to borders and supporting surfaces. #6D001A is the signature oxblood ink for emotional emphasis, while #5B0D18 provides a darker wine tone for depth. #1B1B1F grounds body copy so long-form reading remains comfortable. The palette is intentionally low-saturation and tactile, so the orchid bouquet and burgundy display type carry the romance.

### Layout Paradigm
A magazine-like vertical story rather than a centered landing page. The hero uses a split composition on large screens: copy anchored toward the left with a tall orchid image entering from the right. The letter section uses a narrow reading column offset within a wider paper field. The album becomes an edge-to-edge horizontal filmstrip with visible neighboring frames so the sideways motion is discoverable.

The target design reference is 2392×1080, but the page will scale down fluidly: the hero will preserve a 16:9-ish visual balance on desktop, then become stacked and touch-friendly on smaller screens.

### Signature Elements
1. A fine burgundy vertical rule that appears beside section labels and acts as a quiet editorial anchor.
2. A translucent frosted hero veil that folds upward and blurs as the user scrolls past the opening scene.
3. Slightly varied photo frame proportions, warm matte borders, and offset captions to create a collected-album feeling without an infinite carousel.

### Interaction Philosophy
Interaction should feel like opening a personal letter. Scrolling up collapses the hero in a smooth fold with blur and scale, revealing the message underneath. Scrolling down nudges the album horizontally to the right; scrolling back up moves it left. The gallery is finite and clamped at both ends, never looping. Clicking a frame opens a quiet, centered lightbox that preserves the photograph's natural ratio without filling the entire screen.

### Animation
Use transform and opacity as the main motion properties. The hero starts with a slow 900ms entrance: copy rises a few pixels while the orchid image settles from a slightly larger scale. On scroll, the hero content translates upward, scales subtly toward 0.985, and loses sharpness through a CSS blur interpolation capped at 10px. Album cards move with a spring-like ease-out, but their horizontal offset is bounded by the first and last frame. Lightbox opens from the clicked frame with a 220ms opacity and scale transition beginning around 0.97. All decorative motion is disabled or softened under prefers-reduced-motion.

### Typography System
Use Ciguatera as the display face wherever the browser can load it from the provided font file, with Baskerville Old Style as the poetic editorial fallback for long emotional headlines. Use Gilroy for labels, navigation, and UI metadata. Use Helvetica Neue as the practical body fallback for long reading on systems without Gilroy. The hierarchy is intentionally contrastive: compact uppercase micro-labels, a spacious serif/display title, 18–22px message copy on desktop, and restrained 12–13px album metadata. Avoid Inter.

### Brand Essence
A private birthday letter for Shreyu, made for someone who keeps choosing hope through difficult seasons. Personality: tender, resilient, quietly luxurious.

### Brand Voice
Headlines should sound intimate, certain, and poetic without becoming ornamental. CTAs should be understated and human; microcopy should feel like a note in the margin.

Example lines:
- “For the soul that keeps blooming.”
- “A few moments worth keeping close.”

### Wordmark & Logo
Use a small abstract orchid petal mark made from three asymmetric burgundy petals and one champagne stem, with no text inside the symbol. It should feel like a pressed-flower seal and appear in the hero header and favicon at a visible size.

### Signature Brand Color
Oxblood Burgundy — #6D001A. It is the ownable emotional ink of the experience: warm enough for romance, deep enough for resilience, and distinctive against the ivory paper ground.

### Content and Asset Decisions
The supplied birthday message remains verbatim, with bold emphasis retained around the intended phrases. The gallery will ship with 12 named placeholders: image1.jpg through image12.jpg. The implementation will clearly document that users should place them in `/home/ubuntu/webdev-static-assets/shreyu-birthday/` and upload them through the project asset workflow before publishing. Until then, the UI will show elegant placeholder frames rather than fake personal photographs.
