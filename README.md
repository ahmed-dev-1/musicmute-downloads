# MusicMute Local downloads

Versioned download assets for MusicMute Local on Apple Silicon Macs (macOS 14 or later).

The app downloads separate, checksum-pinned runtime components during Prepare my Mac: Python and ML dependencies, Node, audio tools, the YouTube downloader, Deno, the playback token provider, and the voice processing engine. Each ZIP is removed after its successful installation stage.

Kim Vocal 2 model weights remain at their approved upstream source and are downloaded separately. This repository does not mirror model weights or contain user audio, account data, credentials, or logs.

Downloads are attached to GitHub Releases rather than stored in Git history. Runtime dependencies retain their own licenses and notices.

Current development artifacts are ad hoc signed and are not Apple-notarized public releases.


## Privacy and support

Read the [MusicMute Local privacy policy](PRIVACY.md) for Chrome extension and Mac companion data use, shared YouTube saving, retention and the Chrome Web Store Limited Use disclosure.

[Contact MusicMute support](https://api.music-mute.com/support).
