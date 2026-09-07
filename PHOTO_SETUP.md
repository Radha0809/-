# Photo Setup for Shreyu Birthday

The gallery currently uses elegant visual placeholders so the website can be reviewed without inventing personal photographs. Replace them with the real memories when ready.

## File names

Use exactly these names:

```text
image1.jpg
image2.jpg
image3.jpg
image4.jpg
image5.jpg
image6.jpg
image7.jpg
image8.jpg
image9.jpg
image10.jpg
image11.jpg
image12.jpg
```

## GitHub deployment folder

For GitHub Pages deployment, place the header and personal photos directly in:

```text
client/public/assets/
```

Use `shreyu-purple-orchid-hero.jpg` for the header and `image1.jpg` through `image12.jpg` for the album. The browser paths are `/assets/shreyu-purple-orchid-hero.jpg` and `/assets/image1.jpg` through `/assets/image12.jpg`. Missing photo files stay visually blank until you add them.

## Gallery behavior

The gallery is intentionally finite and does not loop. On desktop, vertical wheel scrolling over the album moves the album horizontally. Scrolling down moves right; scrolling up moves left. On touch devices, swipe horizontally as usual. At either end, the page can continue vertically. Clicking any frame opens a centered lightbox that preserves a comfortable margin around the photograph rather than filling the full screen.

## Replacing the placeholders in code

The placeholder cards are defined in `client/src/pages/Home.tsx` inside the `photos` array. Each item currently has a `file`, `label`, and `ratio`. Each item now has a `/assets/imageN.jpg` `src` field and renders the image inside `.photo-card__placeholder`; if the file is missing, the frame remains blank. The frame sizing and lightbox are already implemented.

## Header Orchid Image

The GitHub-ready header artwork is stored at `client/public/assets/shreyu-purple-orchid-hero.jpg` and is referenced in the website as `/assets/shreyu-purple-orchid-hero.jpg`. It is kept at exactly 2392×1080 and compressed for GitHub deployment. Replace that file with another 2392×1080 image using the same filename to update the hero without changing the code.
