# ask-website

Source of the AskEU website, [ask.eu.com](https://ask.eu.com), in English, German, Polish and Ukrainian.

AskEU is an AI guide that explains healthcare rights in the EU in plain words, with every answer linked to an official source. The website explains the project, shows an interactive preview of how answers are built and lets people ask for early access.

## Technology

- One static page: HTML, CSS and plain JavaScript in a single `index.html`, no framework and no build step
- All four languages are inside the page and switched with JavaScript; the chosen language is remembered in the browser's local storage
- No cookies and no analytics
- On a plain static host, forms do not send data to any server: they prepare the message and open the visitor's own email app
- The live AI prototype needs an AI service. A static copy has none until one is set in `window.ASKEU_CONFIG.aiUrl`
- Fonts (Spectral, Onest, Martian Mono) are loaded from Google Fonts

## Structure

```
index.html            the whole site, all four languages
media/
  askeu-demo-en.mp4   demo video, one per language (en, de, pl, uk)
  askeu-demo-en.vtt   subtitles for each video
  askeu-demo-en.jpg   video poster for each video
  askeu-overview.pdf          project overview (English)
  askeu-responsible-ai.pdf    responsible AI and data protection summary (English)
press/
  askeu-logo.png, askeu-logo-white.png, askeu-symbol.svg   logos for the press kit
  askeu-screenshot-1.jpg ... askeu-screenshot-4.jpg       screenshots
  halyna-mysko-landscape.jpg, halyna-mysko-portrait.jpg   founder photos
```

## View it locally

```sh
git clone https://github.com/askeucom/ask-website.git
cd ask-website
python3 -m http.server 8000
```

Then open http://localhost:8000 in your browser.

## Licence

All rights reserved. See [LICENSE](LICENSE). The code, texts, images, videos and brand assets may not be copied or reused without permission.

The fonts are not part of this repository. Spectral, Onest and Martian Mono are licensed by their authors under the SIL Open Font License 1.1.

## Contact

- Website: [ask.eu.com](https://ask.eu.com)
- Email: [hello@ask.eu.com](mailto:hello@ask.eu.com)
- A wrong or outdated rule on the site: please write to hello@ask.eu.com with a link to the official source.
