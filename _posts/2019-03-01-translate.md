---
apipath: '/translate'
title: 'Translate'
type: 'GET'
---

This endpoint allows (the actual) translating.

### Parameters

#### Required

- `hoster`: The place to host the output video. Available Options: (case-sensitive)
  - `ftp`: Hosts via FTP / Oojmed (https://v.oojmed.com)
  - `imgur`: Hosts via [Imgur](https://imgur.com)

- `lang`: The sign language to translate into. Available Options: (case-sensitive)
  - `BSL`: British Sign Language
  - `ASL`: American Sign Language
  - `DGS`: German Sign Language / Deutsche Gebärdensprache
  - `LSE`: French Sign Language / Langue des Signes Française
  - `LSF`: Spanish Sign Language / Lengua de Signos Española
  - `ISL`: International Sign Language
  - `LSC`: Catalan Sign Language / Llengua de Signes Catalana
  - `Auslan`: Auslan / Australian Sign Language

- `text`: The text to translate.

#### Optional

- `overallSpeed`: Default: `100`. The overall speed of the output video. As a percentage (without %) (`150` = `150%`, `50` = `50%`, etc.). Limit: 50% - 150%.
- `individualSpeed`: Default: `100`. The speed of individual letters (usually when spelling things out). As a percentage (without %) (`150` = `150%`, `50` = `50%`, etc.). Limit: 50% - 150%.
- `quality`: Default `360`. The quality of the output video. Given as a number (`144` = `144p`, `360` = `360p`). Avaliable options:
  - 144
  - 240
  - 360
  - 480

- `redirect`: Default: `true`. Whether to redirect to the URL (`true`) or send it in the response body (`false`).
- `progressKey`: Default: `undefined`. The progress key to send feedback with.

### Response

- If `redirect` is true, the server will redirect (returning a 302 HTTP status code), which will redirect to the uploaded GIF.
- If `redirect` is false, the server will return the uploaded GIF's URL (returning a 200 HTTP status code).
