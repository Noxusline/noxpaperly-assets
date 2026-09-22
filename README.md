# Noxpaperly — remote assets

Public static assets (wallpaper videos + thumbnails + catalog) served to the
**Noxpaperly** Android app over HTTPS. This repo is intentionally **public** so the
app can fetch files by raw URL with no authentication.

## Structure

```
catalog.json      Wallpaper catalog the app reads on launch
videos/           Looping wallpaper videos (mp4, H.264)
thumbs/           Small preview images (jpg) shown in the gallery
```

## URLs (raw)

- Catalog: `https://raw.githubusercontent.com/Noxusline/noxpaperly-assets/main/catalog.json`
- A video: `https://raw.githubusercontent.com/Noxusline/noxpaperly-assets/main/videos/<id>.mp4`
- A thumb: `https://raw.githubusercontent.com/Noxusline/noxpaperly-assets/main/thumbs/<id>.jpg`

## catalog.json format

```json
{
  "version": 1,
  "wallpapers": [
    { "id": "plasma", "name": "Plasma", "category": "Abstract",
      "video": "videos/plasma.mp4", "thumb": "thumbs/plasma.jpg", "free": true }
  ]
}
```

`video` and `thumb` are paths relative to this repo's raw base URL.

## ⚠️ Licensing note

The initial clips are procedurally generated (owned, no third-party rights). Any
Pixabay clips added here are for **testing only** and must be replaced with properly
licensed or owned content before a public Play Store release — a wallpaper app may not
redistribute stock content as its primary product.
