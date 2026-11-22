# SOUND DESK

iPad-first, static broadcast-style sound cue tool for school朗読劇 and live cue operation.

## Open
After GitHub Pages publishes the repository, open:

`https://buturimahura-sys.github.io/simulation0001_buturi/sound-desk/`

The existing root-level project is left unchanged.

## Features
- Broadcast-style hot cue pad grid
- One audio player; one cue at a time
- Sequential cue list with previous / next
- Per-cue audio file, volume, one-shot / loop, fade in / fade out
- Multiple reference images per cue; thumbnail and enlarged preview
- Cue editing, reordering, delete confirmation
- Master volume and immediate master stop
- IndexedDB local project storage
- JSON project export/import containing cue settings, audio and image data
- PWA manifest and service worker for app-shell offline access

## iPad use
1. Open the URL in Safari.
2. Add audio and cue images in CUE EDITOR.
3. Return to LIVE OPERATION and tap a pad to send the cue.
4. Export the project JSON regularly and move that file to another device to restore the project.
5. For a home-screen app, use Safari's Share > Add to Home Screen.

## Data portability
Project export is a self-contained JSON file. Audio and images are embedded as data URLs. This avoids a server and makes transfer between devices possible, but large projects create large JSON files. Store backups in Files/iCloud Drive or another location you control.

## Notes / limitations
- Browser storage is local to each device and browser profile; it does not automatically sync.
- The service worker caches the app shell, not the user's project files. Project export is the portable backup.
- iPadOS may suspend browser audio when the app is backgrounded or the screen locks. Keep Safari/SOUND DESK in the foreground during performance and test the exact iPad + output setup before the show.
- The browser may require a user tap before audio playback. Use the LIVE controls during rehearsal to confirm audio output.
- This is a static browser tool, not a certified broadcast playout system. Always rehearse and keep a separate backup playback option for a live performance.
