# Happily Ever After, Inc.

A funny, mobile-first idle tycoon where fairy-tale businesses become an empire and the Cheshire Cat narrates your adventures.

**v21 · Living Storybook Edition** — sixteen illustrated permanent realms, a weekly event world, and a refreshed interface. No accounts, ads, tracking, paid purchases, frameworks, or build step. Game code lives in `index.html`; the realm artwork is a separate bundled asset.

## Contents

- [Release overview](#release-overview)
- [Upgrade an existing GitHub Pages repository](#upgrade-an-existing-github-pages-repository)
- [First-time hosting](#first-time-hosting)
- [Files in this release](#files-in-this-release)
- [How to play](#how-to-play)
- [The sixteen realms](#the-sixteen-realms)
- [Game systems](#game-systems)
- [Saving and compatibility](#saving-and-compatibility)
- [Technical details](#technical-details)
- [Troubleshooting](#troubleshooting)
- [Validation and limitations](#validation-and-limitations)
- [Development and future releases](#development-and-future-releases)
- [License](#license)

## Release overview

### New in v21: Living Storybook

This cumulative update adds life and feedback to the illustrated game, plus portable save backups. It retains the existing economy, story, world unlocks, production calculations, purchases, managers, upgrades, and rewards.

**Presentation**

- Active, visible shops receive restrained light sweeps and breathing motion. Automated shops have a small green status light; shop names show whether a manager is working, a manual cycle is running, or a tap is needed.
- Successful purchases briefly highlight their shop. Opening a business, reaching a profit milestone, hiring a manager, and opening a realm can show a dismissible celebration card. Buy All produces one representative shop celebration rather than a flood of cards.
- Illustrative currency trails respond to income increases. They travel toward the visible treasury, or toward the quick-purchase controls when the header is offscreen. These visuals do not grant money or represent additional payouts.
- The Cheshire Cat has four matching generated expressions: calm, delighted, winking, and sleepy. Expressions react to purchases, speech, taps, and inactivity. Small portrait motion accompanies the artwork; it is not full skeletal character animation or lip sync.
- Settings adds independent Storybook motion and Celebration cards controls. Device reduced-motion preferences override the new motion. Celebrations remain readable without animation. Hidden pages and offscreen shops avoid the new continuous animation.

**Save & Backups**

Open **Goodies → Save & Backups**, or use its shortcut in Settings. Download a JSON export, choose a save file, or use the copy/paste JSON fallback. Imports are validated and previewed before replacement. The game stores an automatic pre-import backup before writing the imported save. Read the [complete save guide](docs/SAVE-GUIDE.md) before moving progress between devices.

The new export envelope is format 1; the underlying game save remains version 8. Compatible raw saves from our v19/v20 releases are accepted. Earlier incompatible economies, unexpected realm/shop structures, and future formats are rejected rather than silently migrated by the importer. Existing browser saves still use the original loader during an ordinary site upgrade.

**Verification:** 40 isolated checks cover save validation, round trips, review/cancel behavior, storage failures, backup restoration, multi-tab revision handling, action equivalence, motion preferences, and 8,070 unchanged economy values. Generated expression artwork and package assets were inspected. The browser preview could not connect to the local server, so live file-picker/download behavior and physical-phone layout remain unverified.

### Previous release: v20 illustrated world collection

**This release rewires presentation while retaining the game.** It adds individually mapped artwork for **538 permanent shops, 80 guests, and 96 charms**. Original realm names, shop names, manager names, prices, upgrades, unlock requirements, rewards, story content, and save identifiers are retained.

- **Permanent shops:** nineteen realm-specific art sheets give every permanent shop its own illustrated cell, including late-game mystery shops. The final two realms contain 29 shops each in the supplied source; this release preserves those counts.
- **Managers and shop upgrades:** display the associated business illustration to preserve the connection between each manager/upgrade and the shop it affects. These are business illustrations, not new individual manager portraits.
- **Guests:** eighty portrait cells appear both on passing guest buttons and on discovered Guest Book entries. Visitor selection and rewards are unchanged. Portraits are static; the original crossing motion remains, except reduced-motion users receive a stationary visitor with an 11-second expiry.
- **Charms:** all 96 collectibles receive new object illustrations in the album and pack reveal. Unowned charms remain concealed. Rarity, levels, odds, bonuses, and pack timing are unchanged.
- **Currency:** a twenty-cell currency sheet replaces the treasury's generic art with the active realm's currency. The old emoji prefix is removed from the animated cash number, fixing the duplicate gold coin. Price buttons and shop progress labels also use the illustrated currency.
- **Secondary features:** remaining large placeholder pictures on Wishes, Daily Gift, Time Warp, Charm Album, event, and Sequel panels now use illustrated assets.
- **Phone layout:** each shop uses picture-and-name, full-width progress, then purchase-and-statistics rows. Manager and upgrade purchase buttons sit beneath their descriptions on small screens. Compact treasury spacing and smaller scenery height create more room for play. Wide desktop shop screens use two columns.
- **Artwork reference:** open `art-gallery.html` to browse all permanent shop, guest, and charm illustrations with their original names. It does not read or change saves.
- **Manifest:** `assets/art-manifest.json` records the mapping of every illustrated shop, guest, and charm. The game embeds an equivalent compact mapping so it needs no asynchronous manifest download.

**Scope:** weekly-event businesses use the illustrated festival symbol; this release does not create 416 separate shop images for the 52 festivals. Individual manager faces, additional Cat expressions, animation, sound design, and replacement of every decorative or in-text emoji remain future work. Existing story jokes and names are not rewritten.

All 30 newly generated sheets are delivered as high-quality WebP files alongside the four previous PNGs. **Replace the entire assets folder together with index.html.** See `docs/ARTWORK-v20.md` for inventory, mapping, and prompts.

### Previous release: v19 illustrated identity

- **Generated title crest:** an open emerald storybook, fairytale castle, golden crown, and jeweled flourishes replace the original SVG crest. It appears in the header and dialog decoration, and is also the site favicon.
- **Generated interface artwork:** sixteen matching icons supply six bottom navigation destinations, nine Goodies features, contextual screen headings, currency decoration, trophy cards, crossover cards, and global upgrade cards.
- **Generated Cheshire Cat:** a violet-and-turquoise portrait replaces the narrator emoji. The Cat retains its tap interaction and now supports Enter/Space activation.
- **Polished visual system:** coordinated gold trim, emerald and violet accents, cleaner title proportions, a framed treasury, refined business surfaces, parchment dialogs, and updated quick-action and navigation spacing.
- **Contextual headings:** Goodies subpages now show feature-specific titles and illustrations.
- **READY badge fix:** Wishes, Time Warp, and Charms cards show their existing readiness signals correctly. The original card array used the wrong field for its badge.
- **Realm tile fix:** illustrated tiles retain their decoration after changing purchase quantity, which refreshes the header without rerendering the full game.
- **Accessibility:** navigation labels and active-page semantics accompany decorative artwork. Text remains selectable by assistive technology; image assets do not contain UI labels.

This is a complete cumulative release: it includes the previous realm artwork, UI improvements, original game, and all new assets. **Upload the complete assets/ folder with the new index.html.** See [the artwork guide](docs/ARTWORK.md) for the full generation prompts and atlas mapping.

### Foundation retained from v18

This release builds on the original v16 game and the first illustrated environment update (called v17 in this release history). The theme is bright, vivid, whimsical storybook fantasy with elegant typography, jewel-toned surfaces, restrained gold trim, and a modern interface.

### Illustrated realm environments

Each permanent realm receives its own illustration, selected by realm name so the artwork remains matched to the correct world even though atlas order differs from progression order. The same artwork now appears on the realm navigation tiles. Locked realms retain their existing unlock behavior. Weekly events keep their existing event presentation and do not reuse an unrelated permanent realm illustration.

### Full interface styling pass

- Header: a cleaner title area and a separate treasury panel for cash and income information. The header scrolls with the page, leaving more room for the game on small screens.
- Realm navigation: illustrated tiles, clearer selection borders, horizontal scrolling, keyboard activation with Enter/Space, and accessible realm labels.
- Section headings: a title and short explanation above each primary screen.
- Businesses: consistent card spacing, clearer names, progress bars, purchase buttons, and disabled states.
- Managers and upgrades: matching cards, readable descriptions, and larger purchase targets.
- Goodies: refreshed feature cards and a two-column layout on wider screens.
- Stories: updated book headers, icon containers, and reading controls.
- Prestige and events: matching panels, goal tiles, and controls.
- Charms: refined collection tiles with more readable labels.
- Dialogs: warm parchment surfaces, violet actions, softer borders, and scrolling for long content.
- Bottom navigation and quick actions: clearer active states and consistent button shapes.
- Accessibility: visible keyboard focus for buttons and realm tiles; reduced-motion preference suppresses interface animations.

This is a presentation release. It intentionally retains the original economy formulas, unlock rules, story content, rewards, save key, and reset behavior. v20 supplies permanent business illustrations, guest portraits, and charm art. Individual manager portraits and character animation remain future work. Historical sections below describe the earlier foundation.

## Upgrade an existing GitHub Pages repository

1. Download and extract the release ZIP locally. The ZIP contains the site files directly at its root.
2. Back up your current repository or create a commit before replacing files. Close other open game tabs so an older tab cannot write over newer progress.
3. In the folder your existing Pages deployment publishes, replace `index.html` and `README.md` with this release's versions. Add the complete `assets` and `docs` folders, `CHANGELOG.md`, and `.nojekyll`. Keep your repository's existing license and any custom domain `CNAME` file. This package includes the original LICENSE when present in the supplied project.
4. Keep the entire `assets/` folder beside the new `index.html`, including the four previous PNGs, all `shops-*.webp`, `guests-*.webp`, `charms-*.webp`, `currencies.webp`, `cat-expressions.webp`, and `art-manifest.json`. Upload the actual extracted files and folders, not the ZIP itself. Do not add an extra enclosing release folder to the published site.
5. Commit the files. Continue using your existing Pages deployment configuration. If you publish from a `/docs` folder, place **all site files** in that publishing folder; this package's `docs/` directory contains documentation, not the deployment root.
6. Wait for your repository's Pages deployment to complete. Open your existing game URL and refresh. If the old appearance remains, use a hard refresh or close and reopen the tab.
7. Confirm that the crest, Cat expressions, bottom navigation icons, realm banner, and realm tiles show illustrations. Open Goodies → Save & Backups and download a backup file before importing anything. Open Managers, Upgrades, Ever After, Goodies, and Stories to confirm the new interface.

Relative asset paths support both a repository project URL and a custom-domain root. No repository name or username needs to be edited into the source. This package does not change your Pages settings or publish anything automatically.

### Keeping progress during an upgrade

Use the same site address and browser profile. Progress is stored in browser storage rather than in GitHub. Replacing the site files does not intentionally reset it. Switching from a local file to a hosted site, changing domains, using another browser, clearing site data, or using private browsing can give you a different save. The original migration code is retained; this visual release introduces no new save migration. See [Saving and compatibility](#saving-and-compatibility).

### Rollback

Revert the upgrade commit or restore your backed-up site files. Keep the matching assets for whichever version you restore. A rollback of website files is not a backup of browser saves.

## First-time hosting

Extract the ZIP and put its contents in the folder your GitHub Pages site publishes. The entry point must be `index.html`. Use GitHub's Pages deployment appropriate to your repository; a branch-based deployment can publish the root of your chosen branch. After deployment, open your published site URL. No package installation, server-side application, or build command is required.

To preview locally, keep the folder structure intact and open `index.html`. A local HTTP server is preferable for testing hosted behavior. For example, with Python installed, run `python -m http.server 8000` in the extracted site folder and open `http://localhost:8000`. Local preview storage is separate from your live site's storage.

## Files in this release

```text
index.html                      Complete game, styles, and interface logic
assets/realm-atlas.png           Illustrated 4 × 4 realm environment atlas
assets/title-crest.png           Transparent title crest and dialog ornament
assets/ui-icons.png              Transparent 4 × 4 interface icon atlas
assets/cheshire-cat.png          Original transparent narrator portrait
assets/cat-expressions.webp      Four-expression Cat atlas used by v21
assets/shops-*.webp               19 permanent-shop art sheets
assets/guests-*.webp              4 guest portrait sheets
assets/charms-*.webp              6 collectible charm sheets
assets/currencies.webp            20 illustrated currency symbols
assets/art-manifest.json         Complete shop, guest, and charm mapping
art-gallery.html                Optional artwork reference; no save access
README.md                       Current installation and game guide
CHANGELOG.md                    Changes and scope by release
docs/README-v16-original.md      Unmodified original README, for historical reference
docs/ARTWORK.md                  v19 artwork inventory and prompts
docs/ARTWORK-v20.md              v20 inventory, mapping, and prompts
docs/ARTWORK-v21.md              Cat expressions, mapping, and production prompt
docs/SAVE-GUIDE.md               Export/import, backup restoration, and compatibility
docs/VALIDATION-v21.md           Verification scope and remaining manual checks
.nojekyll                       Static-site publishing marker
LICENSE                         Original project license, when supplied
```

The current site is no longer a single-file distribution: distribute `index.html` together with `assets/`. All images load from the same site. There are no remote image or font dependencies.

## How to play

1. Tap a business to start its work cycle and collect its payout when the cycle finishes.
2. Buy additional copies to increase income. Costs rise as ownership grows.
3. Hire its manager to automate production.
4. Buy shop and realm upgrades and reach ownership milestones.
5. Open new realms when you meet their requirements. Tap a locked realm for the current requirements; the game is the authoritative source for costs and reset points.
6. Use Ever After to reset a realm for permanent benefits, and eventually write a Sequel for Golden Quills.
7. Collect gifts, wishes, charms, trophies, event rewards, and story installments along the way.

Bottom tabs: **Shops, Managers, Upgrades, Ever After, Goodies, Stories**. The quick bar provides Work, the next recommended purchase, and Buy All. Goodies contains weekly events, gifts, wishes, time warps, charms, guests, trophies, crossovers, help, and settings.

## The sixteen realms

The table follows permanent-world progression, rather than image-atlas order. Exact unlock requirements and economy values appear in the game.

| # | Realm | Currency | Visual identity |
|---|---|---|---|
| 1 | Storybook Forest | Gold Coins | Emerald woodland, sunbeams, cottages, and a stone bridge |
| 2 | Wonderland | Teacups | Giant pink mushrooms, tea-party gardens, and impossible paths |
| 3 | Arabian Bazaar | Dinars | Turquoise domes, golden sands, palms, and market awnings |
| 4 | Camelot & Sherwood | Crowns | A grand castle, ruby banners, and lush green woods |
| 5 | Olympus Mall | Drachmas | White marble temples floating above luminous clouds |
| 6 | Frostbite Kingdom | Snowflakes | Crystalline ice palace, blue snow, and aurora skies |
| 7 | Neverland | Pixie Dust | Floating tropical islands, pirate ships, and pixie trails |
| 8 | Land of Oz | Emeralds | Emerald spires and a winding yellow brick road |
| 9 | Mermaid Lagoon | Pearls | An underwater palace, coral gardens, and shafts of sunlight |
| 10 | Sugarplum Sweetland | Sugar Cubes | Pink frosting castles, candy canes, and sugar paths |
| 11 | Dragonspine Peaks | Embers | Dramatic volcanic peaks, glowing lava, and a soaring dragon |
| 12 | The Toybox Kingdom | Wind-Up Keys | A wooden toy castle, colorful blocks, and ribbon bunting |
| 13 | The Treasure Seas | Doubloons | Turquoise ocean, a pirate harbor, and golden sails |
| 14 | Hollow Eve | Treats | Violet dusk, glowing pumpkins, and a whimsical haunted village |
| 15 | The Tall Tale Frontier | Silver Dollars | Golden mesas, cacti, and a storybook frontier town |
| 16 | The Nursery at the End of the Hall | Bedtime Stars | A golden moon, floating books, toys, and bedtime stars |

The weekly Event World is separate from these sixteen permanent realms. It uses Event Tickets and changes with the calendar.

## Game systems

### Businesses, managers, and upgrades

Each realm has its own businesses, manager personalities, prices, cycle speeds, upgrade names, and currency. Managers automate individual businesses. Shop upgrades and global upgrades multiply earnings; ownership milestones improve performance. Mystery shops unlock through permanent progression. Work and Buy All help with repeated actions.

### Realm resets and Sequels

Each permanent realm has its own reset currency. Resetting one realm restarts that realm while keeping other realms intact. Storybook Forest awards Glass Slippers; other realms award their own themed points. World Mastery rewards repeated resets. A Sequel is a broader reset that trades slippers for Golden Quills and unlocks Quill Perks. Read the game's confirmation before any reset; this interface release retains those original actions.

### Plot Twists and Crossovers

Plot Twists offer choices with rewards and risks. Their jokes and scenarios fit the current realm. Crossovers reward owning corresponding businesses across several worlds. This release does not rebalance their outcomes or multipliers.

### Weekly events

The rotating festival world has its own shops, ticket economy, medal goals, stamps, and Encore reset. Festival rewards can help the wider game. The existing calendar and thresholds remain in place.

### Gifts, wishes, quests, and time warps

Goodies offers the Wishing Well, Daily Gift streak, daily quests, Flash Days, and Time Warps. Hourglass Sand buys warps through gameplay. Larger warps retain their original confirmation behavior, and event restrictions remain in effect.

### Guests, charms, trophies, and the Cat

Tap visiting guests for rewards and Guest Book progress. Open and collect Lucky Charms for bonuses. Reach goals to earn trophies. The Cheshire Cat reacts to progress and delivers jokes and commentary; tap the Cat for more.

### Stories

Stories unlock through realm progression and other achievements. The Stories tab groups installments by book and offers reading controls. The original README contains historical counts that changed between versions; this release retains the v16 story content rather than promising an older total.

### Numbers and pacing

The game uses compact large-number notation, with a scientific notation option in Settings. Costs, milestone multipliers, diminishing returns, saturation, and reset formulas are retained from the supplied v16 implementation. New artwork does not increase production or change progression speed.

## Saving and compatibility

- Save key: `haec2` in browser `localStorage`; unchanged by this release.
- Autosaving and offline earnings use the existing game implementation.
- Progress is local to the browser profile and site origin. v21 adds manual JSON export/import; there is no cloud synchronization.
- Multiple game tabs can contend for the same save. The original revision guard remains; close older copies while upgrading.
- Opening another repository on the same GitHub Pages hostname may share the same storage key, because browser storage is scoped by origin, not repository path. This release does not alter that existing behavior.
- Keep the same published URL and browser when upgrading. Do not clear site storage as a cache-refresh step.
- Site backups and ZIP releases do not contain a player's browser save. Use Download save file to keep a separate progress backup.
- Before a confirmed import, `haec2_before_import` stores the current progress as a local backup. This backup is separate from the active `haec2` save and can be downloaded or reviewed for restoration.
- Importing restores saved values and resumes now; it does not grant offline catch-up earnings. Already dated boosts, quests, and weekly events continue to follow the current date. The ordinary offline earnings code is unchanged.
- Existing reset and migration behavior remains in the game; this release adds no new reset or conversion.

## Technical details

Plain HTML, CSS, and JavaScript. Static hosting only. The original game loop and signature-based content updates remain. The presentation additions are marked `Illustrated storybook edition`, `v18: Storybook interface system`, and `v19: illustrated identity and modern storybook surfaces`, and `v20: content illustration and mobile readability`, and `v21: Living Storybook` in the stylesheet. `updateRealmIllustration()` selects the environment art; `decorateInterface()` decorates realm navigation and primary screen headings.

The PNG is a 4 × 4 atlas. `illustratedNames` maps its cells to realm names. CSS background positioning selects the relevant cell. Reordering the atlas requires updating this mapping. The original game's `data-w` world themes and realm accent colors continue to drive interface colors.

Artwork was created using built-in image generation, then bundled locally. Art direction: a regular sixteen-panel atlas of bright, vivid, elegant storybook environments with dimensional painted scenery, luminous light, readable landmarks, and no embedded interface text. v20 extends generated artwork to permanent businesses, guests, and charms. Managers and shop upgrades use their associated business artwork. Some inline, event, and decorative symbols remain emoji.

## Troubleshooting

| Symptom | Check |
|---|---|
| Artwork is missing | Confirm all supplied PNG and WebP files in `assets/` were uploaded with matching spelling and case. Check `docs/ARTWORK-v20.md` and `assets/art-manifest.json` for the current inventory. |
| Old UI after an upgrade | Confirm the deployment completed, then hard-refresh the page. Avoid clearing site storage. |
| Site shows a README or a 404 | Confirm Pages publishes the folder containing `index.html`, not the release ZIP or an extra parent folder. |
| Save seems absent | Check the browser profile, domain, and private browsing status. A local preview uses different storage from the live game. |
| Another copy changes progress | Close other tabs or older copies sharing the same site origin. |
| Controls look crowded | Check browser zoom and Settings → Bigger text. The realm strip scrolls horizontally. |
| Weekly event has no painted banner | This release illustrates permanent realms; event-specific artwork is future work. |

## Validation and limitations

See [docs/VALIDATION-v21.md](docs/VALIDATION-v21.md) for the complete scope. JavaScript syntax passes. Forty isolated checks pass, including save round trips, malformed and incompatible file rejection, preview/cancel, backup and active-write failures, restoring the previous backup, newer-tab revisions, reduced-motion behavior, and preserving the save input while income updates. Direct purchases, hiring, upgrades, quick purchases, and Buy All match v20; 8,070 price/cycle/profit values also match.

The expression sheet was visually inspected. Production assets and ZIP contents are checked, and the new image is delivered as quality-96 WebP at its original resolution with transparency.

The preview browser could not connect to the local development server. These tests therefore do **not** verify an actual browser file picker, browser download, animation rendering, phone layout, screen reader, or a full end-to-end playthrough. Test these on your published site using the manual steps in the validation guide. The copy/paste JSON option provides a fallback if your browser does not download files normally.

The new Cat art uses expression swaps and subtle motion; shop movement is a light treatment over existing illustrations. There are no new gameplay rewards, full character rigs, separate manager portraits, event-specific shop illustrations, new sound assets, or cloud synchronization. Earlier artwork and game systems remain included. Some decorative and in-text emoji remain.

## Development and future releases

For every major update, distribute a complete, versioned ZIP with an updated README and CHANGELOG. Document new features, changed files, installation steps, save compatibility, validation, limitations, and rollback. Keep game files and required assets together so each release can be deployed independently.

Possible next art passes: individual manager portraits, richer character animation, themed event shop art, and carefully tuned reward effects. These are roadmap ideas, not implemented features.

The original v16 README is preserved in [docs/README-v16-original.md](docs/README-v16-original.md). Its older counts, unlock tables, single-file instructions, and validation statements describe historical versions and should not override this current guide or the game itself.

## License

The original project README identifies the game as MIT licensed. Preserve the original LICENSE and attribution in your repository. The original documentation is included unmodified for reference. Generated realm artwork is bundled with this release; no new third-party image library or font service was introduced.
