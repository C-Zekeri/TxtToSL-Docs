---
apipath: '/translate'
title: 'Translate'
type: 'GET'
---

This endpoint allows (the actual) translating.

### Parameters

#### Required

- `hoster`: The place to host the output video. Available Options: (case-sensitive, depending on the server's configuration)
  - `ftp`: Hosts via the server's FTP configuration
  - `imgur`: Hosts via [Imgur](https://imgur.com)

- `lang`: The sign language to translate into. Available Options: (case-sensitive, depending on the server's configuration)
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

- `overallSpeed`: Default is set by server configuration, usually: `100`. The overall speed of the output video. As a percentage number (`150` = `150%`, `50` = `50%`, etc.). The server imposes a limit, by default 50% - 150%.
- `individualSpeed`: Default is set by server configuration, usually: `100`. The speed of individual letters (usually when spelling things out). As a percentage number (`150` = `150%`, `50` = `50%`, etc.). The server imposes a limit, by default 50% - 150%.
- `quality`: Default is set by server configuration, usually: `360`. The quality of the output video. Given as a number (`144` = `144p`, `360` = `360p`), the server has a list of options. By default:
  - 144
  - 240
  - 360
  - 480

- `redirect`: Default is set by server configuration, usually: `true`. Whether to redirect to the URL (`true`) or send it in the response body (`false`).
- `progressKey`: Default: `undefined`. The progress key to send feedback with.

### Response

- If `redirect` is true, the server will redirect (returning a 302 HTTP status code), which will redirect to the uploaded GIF.
- If `redirect` is false, the server will return the uploaded GIF's URL (returning a 200 HTTP status code).
