# WAVE Radio — Static Website

Pure HTML, CSS, and vanilla JavaScript. No build step. No npm. No frameworks.

## How to deploy

Upload the entire folder to any web host (cPanel, shared hosting, GitHub Pages,
Netlify drop, etc.) and visit `index.html`. That's it.

You can also double-click `index.html` to open it locally — but the audio
stream and "now playing" metadata only work when the page is served over
`http://` or `https://` (not `file://`).

## Files

```
index.html      Home page
about.html      About page
contact.html    Contact page
style.css       All styles
script.js       Audio player + UI logic
assets/         Show artwork images
```

## Editing content

- Text on each page is in plain HTML — edit `index.html`, `about.html`,
  `contact.html` with any text editor.
- Colors, fonts, spacing live in `style.css` (look for `:root { ... }` at the top).
- Stream servers are listed at the top of `script.js` in the `STREAM_SERVERS`
  array. Edit the URLs there to change which servers appear in the player.
- The "now playing" metadata URL is `METADATA_URL` near the top of `script.js`.

## Notes

- Google Fonts (Inter + Allura) load from `fonts.googleapis.com`.
- The contact form is a demo — it just logs to the browser console and shows
  a toast. To make it actually send mail, point the form's `action` at your
  hosting provider's form handler (e.g. Formspree, Getform, your own PHP
  script in cPanel).
