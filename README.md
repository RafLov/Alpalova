# ALPALOVA website

Static site for https://alpalova.com/, published with GitHub Pages (branch `main`, folder `/`).

- `index.html` is the whole site: Home, Our story, Store and Contact are pages inside it (`#home`, `#story`, `#store`, `#contact`; a product is `#p-<design>-<colour>`). Styles and script are inline.
- `img/` photographs, `fonts/` self-hosted fonts (SIL Open Font License, licences included), `404.html` sends /store, /our-story and /contact to the right page.
- `CNAME` is the custom domain. Keep it as it is.

## Contact form

At the top of `index.html`, `window.ALPALOVA_CONFIG` holds the only settings.

- With `formEndpoint` empty, **Send request** opens the visitor's email app with the request written out for `hello@alpalova.com`, and offers to copy the text.
- With `formEndpoint` set (for example a Formspree address `https://formspree.io/f/xxxxxxxx`), the request is sent from the page and lands in the form service's inbox. For Web3Forms put `https://api.web3forms.com/submit` and the public access key in `accessKey`.

## DNS (at the domain registrar)

| Type | Name | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| AAAA | @ | 2606:50c0:8000::153 |
| AAAA | @ | 2606:50c0:8001::153 |
| AAAA | @ | 2606:50c0:8002::153 |
| AAAA | @ | 2606:50c0:8003::153 |
| CNAME | www | raflov.github.io |

Then Settings, Pages: custom domain `alpalova.com`, and tick **Enforce HTTPS** once GitHub offers it (up to 24 hours after the DNS is in place).
