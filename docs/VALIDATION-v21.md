# v21 validation

## Automated and isolated checks

40 checks pass:

- Economy parity: 538 shops × five ownership levels × three values = **8,070** price, cycle-time, and profit values equal v20.
- Action parity: direct purchases, managers, shop/global upgrades, quick purchases, Buy All, and unaffordable operations produce equivalent game progress in isolated runs.
- Save export/import round trip with nonzero currencies, owned shops, managers, charms, story progress, Time Warps, daily quests, and preferences.
- Compatible raw version-8 save acceptance.
- Invalid JSON, oversized input, wrong checksum, wrong game ID, future formats, missing state, invalid state versions, missing realms/shops, negative cash, wrong flags, invalid cycle progress, unsafe ownership, incorrect upgrade/settings values, unsupported quests, invalid goals, invalid charm/inventory entries, unknown Quill Perks, invalid dates, nonfinite values, and prototype keys are rejected.
- Preview does not write storage or replace state; file labels are escaped; cancellation discards the pending replacement.
- Import saves the prior progress and advances the revision.
- Backup-write failure leaves active progress and its stored save untouched.
- Active-save write failure preserves progress and attempts to restore the prior backup; the tested storage simulation restores it successfully.
- Automatic backup validates and restores; newer other-tab progress is backed up before replacement.
- File/paste/backup controls are present; reduced-motion, hidden-page, and motion-off logic are checked.
- Save input DOM is preserved while production updates continue.
- Fresh-game boot and confirmed-import UI/cache refresh complete in a simulated DOM. Imported ownership and currencies remain intact.

The tests use isolated JavaScript state and simulated storage/DOM; they are not browser end-to-end tests. Syntax and release assets/ZIP integrity are checked separately. Original game action definitions, save schema/key, and game data are retained; presentation wrappers observe successful actions after the original functions execute.

## Artwork and packaging

The generated two-by-two Cat expression sheet was visually inspected: calm, happy, wink, sleepy, with consistent character identity and alpha transparency. It is delivered as quality-96 WebP without a resolution change. Prior production artwork remains bundled. Generated PNG masters stay in the local release working folder and are omitted from the deployable ZIP when a WebP delivery version exists.

## Browser limitation

The browser preview could not connect to the local HTTP server. Live browser downloads, file picking, animation rendering, real phone layout, focus behavior, and screen-reader behavior remain unverified.

## Manual check on the published site

1. Open the existing game URL after deployment. Confirm progress remains and the illustrated assets load.
2. Open an owned manual shop and hire a manager. Confirm labels/status light and production behavior. Scroll away and back; offscreen effects should pause.
3. Make a purchase and cross an ownership milestone. Confirm a readable, dismissible celebration without any additional currency or profit beyond the original rules.
4. Tap the Cat; check expression changes. Leave the game idle to check the sleepy face.
5. Toggle Storybook motion and Celebration cards separately. Also test the device's reduced-motion preference.
6. Download a save. Keep the file. Make a small, recognizable change, then preview the file and cancel; current progress should remain.
7. Import the file, confirm its summary, and check that it restores the exported values. Review the automatic backup and restore it to recover the newer progress.
8. Try an invalid JSON file and check that it is rejected without replacing progress. Test copy/paste JSON if downloading is unavailable.
9. On a phone, check narrow layouts, safe-area spacing, scrollable dialogs, the keyboard with the JSON text box, and uninterrupted editing while automated shops earn.

Export a separate save before performing live restore tests. No live player save was imported or replaced while preparing this release.
