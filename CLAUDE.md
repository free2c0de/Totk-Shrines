# Totk-Shrines

Single-file HTML app (`index.html`) hosted on GitHub Pages at https://free2c0de.github.io/Totk-Shrines/.

## Version tag

`index.html` has a `.version-tag` element (currently rendered as `MM.DD.YYYY vN`, no "Version:" prefix).

**Bump the version number on every single change to `index.html`, no exceptions** — including CSS-only tweaks that seem trivial. This exists specifically because GitHub Pages sits behind a CDN with its own cache window on top of normal browser caching, which previously caused confusion where a fix appeared to do nothing because the live page was actually still serving an older build. A version bump lets you (or the user) confirm via a quick DOM check (`document.querySelector('.version-tag').textContent`) whether the page actually being tested is the one that was just edited, before spending time debugging a "fix" that never deployed.
