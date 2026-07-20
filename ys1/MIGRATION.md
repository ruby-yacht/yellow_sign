# Migration Notes

1. Keep the original repository as a backup.
2. Copy the `stories/`, `shared/`, and `dist/` folders into the repo.
3. Copy the existing cover and audio files into `shared/` as described in the README.
4. Build each story independently with Tweego.
5. After verifying output, move old single-file Twee sources to `archive/legacy-twee/` rather than deleting them.
6. Move generated HTML files into `dist/` once cross-story URLs are updated.
