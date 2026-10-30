# Save & Backups — v21

## Keep a portable copy

1. Open **Goodies → Save & Backups**. Settings also links here.
2. Select **Download save file**. Your browser downloads a dated `.json` file containing a snapshot of your current game.
3. Keep this file somewhere you control. You can move it to another device yourself.
4. If your browser cannot download a file, expand **Copy or paste save JSON**, choose **Show current save JSON**, and copy all the text into a text file. This is the same export data.

No account, server upload, clipboard permission, or cloud service is used. This is manual transfer, not automatic synchronization. An export includes game progress and supported settings, including number notation.

## Import on this or another device

1. Open this release's game on the destination device.
2. Open Save & Backups and choose a JSON file, or paste its complete contents into the text box and select **Review pasted save**.
3. Check the summary: worlds, businesses, Glass Slippers, Golden Quills, and story parts read.
4. Choose **Keep my current progress** to cancel, or **Replace progress with this save** to proceed. Reviewing a save does not replace anything; the current game can continue earning while you review.
5. Before replacement, the game stores a local backup of the progress you are leaving. If backup storage or writing the active save fails, the in-memory game is not replaced.
6. A successful import returns to Settings. You can return to Save & Backups to download the automatic backup or to restore it.

Close other open copies before importing. Existing revision guards are retained, and the importer advances the revision beyond the active stored save. If another tab has newer progress when you confirm, that newer stored progress is selected for the automatic backup.

## Restore the automatic backup

Expand **Automatic backup before an import**. You can download that backup as a JSON file, or review it and explicitly confirm restoration. Restoration uses the same validation and confirmation as any import, and makes the progress you are leaving the new automatic backup.

Only one pre-import backup is kept locally. Repeated imports replace it. Export important points in your story to separate files. Browser storage, including this backup, can disappear if site data is cleared or a private browsing session ends. A website ZIP is not a player-save backup.

## Time and events

An imported file restores the values stored in it and resumes at the current time. **Import does not grant offline catch-up earnings.** Existing time-limited boosts retain their original expiry dates. Daily quests and weekly events follow the current calendar, using the game's existing rollover behavior. Ordinary closing/reopening offline earnings are unchanged.

## Supported files

- v21 JSON exports: game ID `happily-ever-after-inc`, export format 1, underlying state version 8.
- Compatible raw state JSON from the v19/v20 game, with seventeen realm entries and the current shop/upgrade structure.
- The local automatic pre-import backup, which uses the same export envelope.
- Maximum selected file size or pasted JSON length: 2 MB. Normal exports are substantially smaller.

The importer rejects unexpected game IDs, future export formats, older incompatible game states, wrong realm/shop/upgrade counts, malformed JSON, invalid numbers or flags, unsupported quest IDs, invalid inventory entries, and unsafe object keys. It does not silently apply the original economy migration to imported files.

The export checksum detects accidental changes to the state payload. It is not encryption, authentication, or an anti-cheat mechanism. Raw legacy saves have structure checks but no export checksum. Manually editing or rearranging the payload can invalidate an export checksum.

## Storage and privacy

| Key | Purpose |
|---|---|
| `haec2` | Original active game save; unchanged |
| `haec2_before_import` | One local backup before a confirmed import |
| `haec_note` | Existing number-notation preference |

Browser storage is scoped to the site origin. Different repository paths on the same GitHub Pages hostname can share these keys, as with the original game. Different domains, browsers, profiles, and private sessions can have separate saves. Export/import gives you a deliberate way to move progress between them.

## If something does not work

- **Unreadable file:** select the JSON export, not the website ZIP or an image.
- **Checksum mismatch:** use an intact exported copy. The game leaves active progress unchanged.
- **Incompatible structure/version:** use a compatible release to open the original save, or keep playing the existing browser save. Do not alter the version number to bypass checks.
- **Storage unavailable/full:** export current progress first, and resolve browser storage availability. The importer requires both backup and active-save writes to succeed.
- **File downloads unavailable:** use Show current save JSON and manually copy the text.
- **No automatic backup:** it is created when you confirm an import, not merely by exporting or previewing.

Browser file-picker and download behavior still need live verification on the target device; the underlying validation and storage paths have isolated automated coverage.
