# Regex Cheatsheet and Playground

A regex cheatsheet, a live tester with match highlighting, and a library of common tested patterns, in one page. No server, no tracking, no third-party scripts.

**Live demo:** https://0xelitesystem.github.io/regex-cheatsheet-playground/

## Use

Open `index.html` in any modern browser, or visit the GitHub Pages link in the repo description.

- Type a pattern and toggle flags (`g`, `i`, `m`, `s`, `u`, `y`). Matches highlight in the test text as you type.
- Capture groups and named groups show up in a table below the highlights.
- Click any pattern in the library (Email, URL, IPv4, Date, Slug) to load it into the tester with sample text and a plain-language description.
- Scroll to the cheatsheet for the common tokens grouped by purpose.

An invalid pattern shows the engine's error message inline and never crashes the page. Zero-length matches (for example an empty alternation with the `g` flag) are handled safely so the tester cannot get stuck in an infinite loop.

### Flavor note

This uses the **JavaScript / ECMAScript** regex flavor, the same engine your browser runs. Other flavors (PCRE, Python `re`, Go, .NET) differ in lookbehind support, named-group syntax, and some escapes, so patterns that pass here will not always behave identically elsewhere.

The library patterns are pragmatic, not exhaustive. Email in particular cannot be fully validated by a simple regex; the included pattern covers common cases.

## Why this exists

Most regex helpers make you choose between a reference and a tester. This puts the cheatsheet, a live tester, and a set of ready-to-use patterns on one page, with no dependencies and nothing sent to a server.

## Privacy

Everything runs in your browser. The pattern and test text never leave your machine. Verify by viewing the page source or by opening DevTools and watching the network tab, no requests are made.

## Run locally

```bash
git clone https://github.com/0xelitesystem/regex-cheatsheet-playground
cd regex-cheatsheet-playground
# Open index.html in your browser, or:
python -m http.server 8000
```

## Build

There is no build. It is a single HTML file.

## License

MIT.

## Related

- [regex-tester](https://github.com/0xelitesystem/regex-tester), a focused regex tester
- [regex-tester-with-explainer](https://github.com/0xelitesystem/regex-tester-with-explainer), test and explain a pattern token by token
- [gradient-generator](https://github.com/0xelitesystem/gradient-generator), build CSS gradients visually
