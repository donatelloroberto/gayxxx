# GayVN SkyStream Converted Repository

Converted from `gayvn-cs-main.zip`.

## Converted providers

- BestHDgayporn — https://besthdgayporn.com
- BoyfriendTV — https://www.boyfriendtv.com
- Fxggxt — https://fxggxt.com
- Gaycock4U — https://gaycock4u.com
- GayStream — https://gaystream.pw
- Gayxx — https://gayxx.net
- GEPorner — https://www.eporner.com
- GPornOne — https://pornone.com/gay
- GPorntrex — https://www.porntrex.com
- GXtapes — https://gay.xtapes.in
- HDgay — https://hdgay.net
- Jayboys — https://javboys.tv
- Justthegays — https://justthegays.com
- Nurgay — https://nurgay.to
- topHDgayporn — https://tophdgayporn.com
- Xhamster — https://vi.xhspot.com/gay

## Use in SkyStream

After uploading this folder to `donatelloroberto/gayvn-cs` branch `skystream`, add this repository URL in SkyStream:

```text
https://raw.githubusercontent.com/donatelloroberto/gayvn-cs/skystream/repo.json
```

## Structure

```text
repo.json
plugins/<Provider>/plugin.json
plugins/<Provider>/plugin.js
dist/<packageName>.sky
dist/plugins.json
conversion-report.json
```

## Stream extraction

Each converted plugin exposes these SkyStream functions:

- `getHome(cb)`
- `search(query, cb)`
- `load(url, cb)`
- `loadStreams(url, cb)`

The generated `loadStreams` searches:

- direct `.mp4`, `.m3u8`, `.webm` URLs
- JSON-LD `contentUrl`, `embedUrl`, and script variables
- `<video>` and `<source>` tags
- `href`, `src`, `data-src`, `data-video`, `data-file`, `data-hls`, `data-mp4`
- nested iframe players up to depth 2
- common CloudStream-style embedded player pages

## Local test notes

SkyStream generally expects remote raw GitHub URLs. The generated manifests are already written for:

```text
https://raw.githubusercontent.com/donatelloroberto/gayvn-cs/skystream/
```
