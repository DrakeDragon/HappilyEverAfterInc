# Changelog

## v21 — Living Storybook Edition

### Added
- Active shop light/breathing effects, automated status lights, and readable activity labels.
- Successful purchase highlights and dismissible business-open, ownership-milestone, manager-hired, and realm-open celebration cards.
- Throttled illustrative currency trails toward the visible treasury or quick-purchase controls; no new earnings or rewards.
- Four generated Cat expressions (calm, delighted, wink, sleepy), reaction hooks, and subtle portrait motion.
- Independent motion/celebration preferences, reduced-motion support, hidden-page/offscreen controls, and capped temporary effects.
- Goodies → Save & Backups, linked from Settings: downloadable JSON exports, file import, manual JSON fallback, import preview/cancel, validation, and a pre-import backup with download/restore.
- Export format 1 with game identifier and payload checksum; underlying state remains version 8.
- Save portability guide, verification guide, and expression artwork prompt documentation.

### Save behavior
- Active save key remains haec2; local pre-import backup uses haec2_before_import.
- Compatible raw v19/v20 states can be imported; incompatible states are rejected.
- Both backup and active-save writes must succeed before replacing in-memory progress.
- Revisions advance beyond the stored active revision; newer other-tab progress is chosen for the backup.
- Imports resume at the current time without granting offline catch-up earnings. Normal offline code and calendar rollover rules remain.
- Save text/file input stays mounted while the economy updates.

### Retained
- Existing shops, progression, story, calculations, action functions, prices, production speed, and rewards. Feedback wrappers run after successful original actions.
- All prior production artwork, including the v20 shop, guest, charm, and currency collection.

### Validation
- 40 isolated checks pass, including 8,070 unchanged economy values, action parity, save round trips, adversarial validation, cancellation, quota/write failure handling, automatic restoration, revision handling, and motion preferences.
- JavaScript syntax, expression artwork, assets, and ZIP integrity checked.
- Local browser preview connection failed. File-picker/download behavior and physical-phone layout remain unverified; see docs/VALIDATION-v21.md.

## v20 — Illustrated World Collection

### Artwork
- 538 individually mapped permanent-shop illustrations across 19 realm-specific sheets.
- 80 guest portraits across 4 sheets, used for passing guests and discovered Guest Book entries.
- 96 charm illustrations across 6 sheets, used in the album and pack reveals.
- One twenty-cell currency sheet for realm currency and secondary resources.
- Managers and shop upgrades display the associated business art.
- Large secondary feature symbols now reuse existing illustrated UI art.
- Optional art-gallery.html and a complete assets/art-manifest.json mapping.

### UI and UX
- Fixed duplicate treasury currency: removed the old emoji prefix and replaced the generic decoration with realm-specific currency art.
- Replaced currency emoji in shop prices and progress labels with illustrated symbols.
- Phone shop layout separates identity, progress, and purchase rows; manager/upgrade buttons use a separate row.
- Tighter phone treasury and scene layout; two-column desktop shops.
- Passing guest buttons have accessible names and a stationary, expiring reduced-motion variant.
- Mystery shops and unowned charms retain their concealed presentation.

### Game compatibility
- Existing game data and save key retained.
- Prices, cycle times, and profits match v19 for all 538 shops at five ownership levels (8,070 checked values).
- Shop, guest, charm, and prestige data unchanged, including guest reward definitions.
- Presentation adapters replace image markup; gameplay actions, progression, story content, and economy formulas are retained.
- No player-save reset or new migration introduced.

### Validation
- Syntax, atlas mappings, concealed/revealed states, legacy coin removal, local asset references, images, and ZIP integrity checked.
- Original game-action functions compared for unintended edits.
- Generated atlases inspected for grid layout and subject coverage.
- Live browser and physical-phone visual testing remain outstanding; no complete end-to-end gameplay audit claimed.

### Remaining scope
- Unique manager portraits, event-specific shop art, Cat/guest character animations, sound design, and remaining decorative/text emoji.
- Event businesses use a shared illustrated festival icon; managers/upgrades use their associated shop's illustration.

## v19 — Illustrated Identity Edition

### Added
- Custom generated transparent crown, castle, and storybook title crest, also used on dialogs and as the favicon.
- Custom generated sixteen-cell transparent interface icon atlas.
- Custom generated static Cheshire Cat portrait, with keyboard activation for the narrator card.
- Illustrated navigation, Goodies cards, contextual headings, currency decoration, trophies, crossovers, and global upgrades.
- Full artwork inventory and generation prompts in docs/ARTWORK.md.

### Changed
- Title layout and crest proportions, treasury panel, narrator card, menu cards, business surfaces, book panels, parchment dialogs, quick actions, and navigation spacing.
- Feature-specific headings for Wishes, Time Warp, Charms, Guests, Trophies, Crossovers, Help, and Settings.
- README updated with current asset requirements and cumulative installation instructions.

### Fixed
- Goodies READY badges read the correct readiness field.
- Quantity-only header refreshes reapply realm tile illustrations and accessibility decoration.

### Compatibility
- No new save key, migration, economy formula, story content, or game reward changes.
- No intentional edits to original purchase, work, hire, upgrade, reset, or save functions.
- Upgrade index.html and the complete assets folder together. Keep your existing domain, browser profile, CNAME, and repository license.

### Validation
- Node JavaScript syntax check passed.
- Focused render checks passed for sixteen icon mappings, six navigation destinations plus event selection, header redecoration, nine feature cards, and READY badge on/off states.
- PNG dimensions and alpha transparency inspected; local asset paths checked; ZIP integrity verified.
- Original game-action functions compared against v18 for unintended edits.
- Live browser visual verification and full end-to-end gameplay testing remain outstanding. Generated artwork was inspected directly.

### Scope remaining
Individual shop, manager, guest, and collectible artwork; Cat animation; event-specific environments; sound design. Existing emoji remain in those areas.

## v18 — Storybook Interface Edition

- Complete interface styling pass covering treasury, realm selector, primary headings, business cards, managers, upgrades, Goodies, Stories, prestige panels, events, charms, dialogs, notifications, and bottom actions.
- Illustrated realm navigation using the bundled environment atlas.
- Keyboard activation and labels for realm tiles, visible button focus, and broader reduced-motion styling.
- Compact-screen spacing and wider-screen Goodies grid.
- Detailed deployment, upgrade, save compatibility, rollback, troubleshooting, and release documentation.
- Original README preserved under docs; original LICENSE retained where supplied.
- No intentional changes to game economy, unlock rules, story content, save key, or reward calculations.

### Validation

- JavaScript syntax check passed using Node.
- Required package paths and original save key checked.
- Browser verification could not be completed: the preview browser timed out reaching the local server. Visual and interactive browser checks remain outstanding.
- Full late-game and economy regression testing not performed.

## v17 — Illustrated environment foundation

The first visual edition introduced a sixteen-realm environment atlas, realm scene banners matched by name, and initial business-card and responsive-layout refinements. This release number names that earlier unnumbered visual edition for documentation continuity.

## v16 — Original supplied game

See docs/README-v16-original.md for the original release guide and its historical version notes.
