# Yellow Sign — Clean Source Layout

This archive reorganizes the current repository's active Twee sources into one folder per independently compiled story.

## Structure

- `stories/king-in-yellow/` — The King in Yellow play
- `stories/home/` — Home story
- `stories/city/` — City story
- `shared/images/` — shared images (copy `images/cover.png` here)
- `shared/audio/` — shared audio (copy `audio/Descend.mp3` here)
- `dist/` — compiled HTML output

Each story keeps exactly one `StoryTitle`, one `StoryData`, and one `StoryInit`. Passages are separated by purpose.

## Build with Tweego

From the repository root:

```sh
tweego stories/king-in-yellow -o dist/king-in-yellow.html
tweego stories/home -o dist/home.html
tweego stories/city -o dist/city.html
```

The existing cross-story links expect `home.html` and `city.html`. You can either compile those names in the repository root or update the targets to `dist/home.html` and `dist/city.html`.

## Asset migration

Copy these existing repository files:

```text
images/cover.png       -> shared/images/cover.png
audio/Descend.mp3      -> shared/audio/Descend.mp3
```

The King in Yellow source now uses the correct case-sensitive filename `Descend.mp3`.

## Why this layout

- Story configuration is easy to find.
- Shared initialization code is isolated.
- Acts and rest passages are independently editable.
- Separate stories cannot accidentally merge their `StoryData` or passage namespaces.
- Compiled HTML is kept out of source folders.
