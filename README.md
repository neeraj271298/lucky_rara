# Lucky Rara Website — YouTube Embed Fixed

This version fixes YouTube embedded-player Error 153 by explicitly preserving the HTTP Referer and passing the live site origin to each YouTube iframe. It keeps the three Shorts and three featured videos already configured.

## Deploy on Netlify
Upload the contents of this project folder (the folder containing `index.html`, `css/`, and `js/`) or upload the ZIP and extract it before deploying.


## Local testing

Do **not** open `index.html` directly with `file://` if you want YouTube embeds to play. YouTube requires an HTTP `Referer` for embedded playback; a `file://` page normally has no HTTP Referer, which causes Error 153.

From this project folder run:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

On a normal HTTP/HTTPS page, the website sends the recommended `strict-origin-when-cross-origin` referrer policy and YouTube origin parameter.
