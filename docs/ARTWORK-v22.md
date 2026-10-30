# v22 header artwork and animation

New assets created with built-in image generation and delivered as quality-95 WebP at their original dimensions. PNG masters remain in the local release folder; the deployable ZIP uses the WebP files.

## Title panorama

`assets/title-panorama.webp`: 2172 × 724, RGB. A wide cinematic fantasy environment under a dark readability overlay, with live HTML title text above it. Gentle pan/zoom pauses with Storybook motion off, hidden-page handling, or reduced-motion preferences.

## Book sprite

`assets/title-book-sprite.webp`: 1774 × 887, RGBA, four columns × two rows. Eight sequential page-turn poses. CSS holds the resting pose, plays the page-turn sequence near the end of each eight-second loop, and adds subtle floating motion. The existing `title-crest.png` is displayed until the sprite image loads. The title words remain live text; this is a sprite-animated emblem with separate title and atmosphere layers, not a prerecorded video.

## Prompts

### v22Backdrop

Premium original whimsical storybook fantasy game title backdrop, wide cinematic 3:1 panorama. An elegant gilded open storybook in lower foreground, luminous emerald fairytale castle on floating garden island to the right, sapphire twilight sky, turquoise magical river, warm gold windows, pink flowering trees and floating gold motes. Bright vivid luxurious dimensional painted game art, restrained sophisticated composition. Left half mostly clean deep teal and midnight-blue atmosphere reserved for live title text overlay, all focal scenery on right third and lower corners, no text, letters, logos, UI, or borders. Enchanting, elegant, modern, richly lit, not scary.

### v22Sprite

Production animation sprite atlas, exactly 4 columns by 2 rows, eight equal square cells on truly transparent background. One identical small sculptural open emerald storybook with gold page edges, gold crown hovering above and tiny emerald star, centered at identical scale in every cell with generous 15 percent padding. Bright premium whimsical dimensional painted game UI asset. Eight sequential frames of ONE gentle looping book-page turn: frames1 closed-to-flat open resting book, frames2-4 single luminous ivory page rises and turns from right to left, frames5-7 page settles leftward, frame8 returns to same open resting pose as frame1. Keep cover, crown, lighting, camera and location identical; only single page shape and restrained sparkles move. Front three-quarter view, bold readable silhouette at80pixels, all content fully inside eachcell. No backgrounds, no labels, numbers, lettering, grids, or text. Exact regular 4x2 grid, no gutters.
