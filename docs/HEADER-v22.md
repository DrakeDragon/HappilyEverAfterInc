# v22 animated storybook header

## Structure

1. Title stage: live title typography above a new painted panorama. An emerald book/crown emblem uses an eight-frame page-turn sprite, gentle floating motion, and separate star accents. The resting pose is held between page turns.
2. World atlas: full-name destination cards for all sixteen permanent realms and the weekly festival. Locked worlds remain clickable to show their original requirements. Side controls scroll the rail; changing realms centers the selected card. Quantity-only refreshes preserve rail position.
3. Treasury: current realm, chapter, active/resting income state, a single currency image, available balance, and income per second. Additional cells show Glass Slippers/global bonus, local reset points and bonus (or open businesses in Forest), and Golden Quills. Festival Favors replace local prestige information in the event world. Active profit boosts have a separate row.
4. Purchase quantity: existing ×1/×10/×100/MAX behavior with a dedicated label.
5. Bonuses and discoveries: the original pills remain available inside an expandable section.

The older standalone realm scene is hidden to avoid a second large scenery block. Realm artwork is retained in the atlas cards and signet. Gameplay controls and bottom navigation remain unchanged.

## Eight decimal places

`fmtC()` renders eight fractional digits for balances and per-second income. Examples:

- `4.12500000`
- `1.23456789K`
- `1.00000000M`
- `1.23450000e4` with scientific notation enabled

Rounding near a suffix boundary advances to the next suffix, rather than showing 1000 under the prior suffix. The main price formatter remains unchanged.

The existing cash animation still moves the displayed value toward actual cash and immediately reflects decreases from purchases. It writes into the new `cash-value` element only when the formatted text changes. No game-state values are changed by formatting or interpolation. No synthetic money or random decimal digits are added. The display can settle when income stops or an increment is below display/numerical precision.

## Accessibility and motion

- Destination controls are native buttons, with full accessible names and active selection state. Locked controls intentionally remain enabled so their requirements can be read.
- Rail arrows have 44-pixel minimum targets.
- The title words are live HTML text, not baked into the image.
- Static crest fallback remains until the sprite image loads.
- Sprite, floating, panorama, and star animation follow Storybook motion and reduced-motion settings. Hidden-page handling pauses the new motion.
- The rapidly changing balance is not an assertive live region.

## Automated scope

48 total isolated checks pass: the 40 prior save/game/presentation checks plus eight new header checks. Header checks exercise small/large/zero balances, rounding transitions, scientific notation, seventeen original destination actions and labels, retained prestige/boost readouts, and interpolation with unchanged actual money. Simulated boot and import refresh still pass. These checks do not measure real rendered geometry or animation smoothness.

## Manual review on the published site

- Check the header at phone widths around 320–430 pixels and at desktop width. Verify eight fractional digits fit without clipping.
- Switch among Forest, Wonderland, a late realm with a long name, and the festival; verify currency, title, and local bonus labels update.
- Tap a locked world and confirm its original requirement dialog appears. Test keyboard selection and rail arrows.
- Change purchase quantity and confirm it does not reset the rail or change game costs.
- Watch the resting book and page-turn sequence. Turn Storybook motion off and test device reduced-motion preferences.
- Verify the balance settles when no income arrives, decreases on purchases, and changes smoothly with income. Compare scientific and compact notation.
- Expand Bonuses & discoveries, use save export/import, and check the bottom controls still work.

The local preview connection was unavailable in earlier testing; live browser and physical-device validation remain outstanding for this release.
