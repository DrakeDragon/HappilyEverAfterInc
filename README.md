# Happily Ever After, Inc.

A funny, mobile-first idle tycoon where fairy-tale businesses become an empire and the Cheshire Cat narrates your adventures.

**v18 · Storybook Interface Edition** — sixteen illustrated permanent realms, a weekly event world, and a refreshed interface. No accounts, ads, tracking, paid purchases, frameworks, or build step. Game code lives in `index.html`; the realm artwork is a separate bundled asset.

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

This is a presentation release. It intentionally retains the original economy formulas, unlock rules, story content, rewards, save key, and reset behavior. Custom business illustrations, character portraits, and animation are still future work; existing emoji remain in those areas.

## Upgrade an existing GitHub Pages repository

1. Download and extract the release ZIP locally. The ZIP contains the site files directly at its root.
2. Back up your current repository or create a commit before replacing files. Close other open game tabs so an older tab cannot write over newer progress.
3. In the folder your existing Pages deployment publishes, replace `index.html` and `README.md` with this release's versions. Add the complete `assets` and `docs` folders, `CHANGELOG.md`, and `.nojekyll`. Keep your repository's existing license and any custom domain `CNAME` file. This package includes the original LICENSE when present in the supplied project.
4. Keep `assets/realm-atlas.png` exactly at that relative path beside the new `index.html`. Upload the actual extracted files and folders, not the ZIP itself. Do not add an extra enclosing release folder to the published site.
5. Commit the files. Continue using your existing Pages deployment configuration. If you publish from a `/docs` folder, place **all site files** in that publishing folder; this package's `docs/` directory contains documentation, not the deployment root.
6. Wait for your repository's Pages deployment to complete. Open your existing game URL and refresh. If the old appearance remains, use a hard refresh or close and reopen the tab.
7. Confirm that the realm banner and realm tiles show illustrations. Open Managers, Upgrades, Ever After, Goodies, and Stories to confirm the new interface.

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
README.md                       Current installation and game guide
CHANGELOG.md                    Changes and scope by release
docs/README-v16-original.md      Unmodified original README, for historical reference
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
- Progress is local to the browser profile and site origin; there is no cloud synchronization.
- Multiple game tabs can contend for the same save. The original revision guard remains; close older copies while upgrading.
- Opening another repository on the same GitHub Pages hostname may share the same storage key, because browser storage is scoped by origin, not repository path. This release does not alter that existing behavior.
- Keep the same published URL and browser when upgrading. Do not clear site storage as a cache-refresh step.
- Site backups and ZIP releases do not contain a player's browser save.
- Existing reset and migration behavior remains in the game; this release adds no new reset or conversion.

## Technical details

Plain HTML, CSS, and JavaScript. Static hosting only. The original game loop and signature-based content updates remain. The presentation additions are marked `Illustrated storybook edition` and `v18: Storybook interface system` in the stylesheet. `updateRealmIllustration()` selects the environment art; `decorateInterface()` decorates realm navigation and primary screen headings.

The PNG is a 4 × 4 atlas. `illustratedNames` maps its cells to realm names. CSS background positioning selects the relevant cell. Reordering the atlas requires updating this mapping. The original game's `data-w` world themes and realm accent colors continue to drive interface colors.

Artwork was created using built-in image generation, then bundled locally. Art direction: a regular sixteen-panel atlas of bright, vivid, elegant storybook environments with dimensional painted scenery, luminous light, readable landmarks, and no embedded interface text. Existing business and character emoji are retained.

## Troubleshooting

| Symptom | Check |
|---|---|
| Scene artwork is missing | Confirm `assets/realm-atlas.png` exists in the publishing folder and its spelling and case match. |
| Old UI after an upgrade | Confirm the deployment completed, then hard-refresh the page. Avoid clearing site storage. |
| Site shows a README or a 404 | Confirm Pages publishes the folder containing `index.html`, not the release ZIP or an extra parent folder. |
| Save seems absent | Check the browser profile, domain, and private browsing status. A local preview uses different storage from the live game. |
| Another copy changes progress | Close other tabs or older copies sharing the same site origin. |
| Controls look crowded | Check browser zoom and Settings → Bigger text. The realm strip scrolls horizontally. |
| Weekly event has no painted banner | This release illustrates permanent realms; event-specific artwork is future work. |

## Validation and limitations

The release script passes JavaScript syntax validation. Packaging checks confirm relative artwork references, the original save key, and the required release files. The preview browser could not connect to the local server, so visual and interactive checks remain outstanding. Details are recorded in `CHANGELOG.md`; no claim is made that every late-game progression path has been tested.

This is a major UI styling pass, not a finished AAA production. Business icons and characters still use the original emoji. No new character animation, sound design, cloud save, or custom event artwork is included. Long-term economy balance is inherited from v16 and has not been re-simulated.

## Development and future releases

For every major update, distribute a complete, versioned ZIP with an updated README and CHANGELOG. Document new features, changed files, installation steps, save compatibility, validation, limitations, and rollback. Keep game files and required assets together so each release can be deployed independently.

Possible next art passes: individual business illustrations, a custom Cheshire Cat portrait and expressions, a coordinated icon set, themed event art, and carefully tuned reward effects. These are roadmap ideas, not implemented features.

The original v16 README is preserved in [docs/README-v16-original.md](docs/README-v16-original.md). Its older counts, unlock tables, single-file instructions, and validation statements describe historical versions and should not override this current guide or the game itself.

## License

The original project README identifies the game as MIT licensed. Preserve the original LICENSE and attribution in your repository. The original documentation is included unmodified for reference. Generated realm artwork is bundled with this release; no new third-party image library or font service was introduced.
