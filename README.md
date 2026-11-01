# 🔍 shURLock

**The consulting link detective.** A free, no-sign-up URL shortener and QR code generator
that inspects every link for disguises before it shortens it.

## [▶ Try it now](https://erickb2021-lgtm.github.io/shurlock/)

---

## Features

- **Shorten a link** with your own custom ending (5–30 characters)
- **Generate a QR code** (a separate tool) with ink colours, sizes, and PNG download
- **Fishy-link detection** with an animated *Deduction Report*
- **Case files** of your recent and past links: Visit, QR, Share, Copy
- **Atmosphere:** Baker Street at dusk, gaslight, fog, rain, a magnifying glass that reveals hidden clues, and Sherlock peeking over the bottom of the page

## What gets blocked

- Anything that isn't `http://` or `https://` (like `javascript:` links)
- The `real-site.com@evil.com` trick
- Raw IP addresses and local addresses
- Brand look-alikes: `paypa1`, `g00gle`, `gooogle`, `paypal-login.com`
- Foreign look-alike letters (punycode) and invisible characters
- Other link shorteners (no hiding a link behind two short links)
- Domains stuffed with words like `secure-login-verify`
- `.zip` / `.mov` domains and direct program downloads (`.exe`, `.apk` …)
- Custom endings that look like a bank, login, or brand page

## How it works (routing, IDs, persistence)

- **IDs:** each link gets a random 6-character code from `a–z0–9` (about 2.1 billion possibilities), or your custom ending.
- **Persistence:** links are saved in your browser's `localStorage`.
- **Routing:** GitHub Pages shows `404.html` for any address that doesn't exist, so visiting
  `…/shurlock/your-ending` loads `404.html`, which looks up the ending and redirects you.
- **Note:** links are stored in your browser, so they open on the device that created them.

## Disclaimer

shURLock is a free learning project provided "as is". Its checks catch common disguises, but no automated
check can guarantee a site is safe. Not affiliated with TinyURL or any Sherlock Holmes film, TV, or publishing
rights holder; Conan Doyle's original stories are in the public domain. QR generation uses
[qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) (MIT).

## License

MIT
