# Product Demos

Working previews of Moorepay Payroll features, published as plain HTML on GitHub Pages so anyone with the link can open them without an account.

Live site: `https://<github-username>.github.io/product-demos/` (set once GitHub Pages is switched on, see below).

## Layout

```
index.html            the hub page: one card per demo
feedback.html         sends "Give feedback" clicks to a Microsoft Form (paste the form link in here)
<demo-name>/index.html   one folder per demo, self-contained HTML
robots.txt, .nojekyll    keep search engines out and stop GitHub processing the files
```

## Adding a demo (for Claude or a person)

1. Build the demo as a single self-contained HTML file (inline CSS and JS, made-up data only, never real customer data).
2. Wrap it with the standard head: `<meta name="robots" content="noindex, nofollow">`, a `<title>` ending in "- Roadmap preview", and the floating "Give feedback" button that links to `../feedback.html?demo=<demo-name>`. Copy the pattern from `home-screen/index.html`.
3. Save it as `<demo-name>/index.html` using a short lower-case name with hyphens, e.g. `ai-pay-run-summary`.
4. Add a card for it to `index.html` (title, one line on what it shows, date added).
5. Commit and push to `main`. GitHub Pages publishes within a minute or two.
6. The link to put on the epic is `https://<github-username>.github.io/product-demos/<demo-name>/`.

Rules: every demo carries the "Roadmap preview - subject to change" banner, uses fictional data, and names no dates.

## One-off setup

1. Create a public repo called `product-demos` on GitHub and push this folder to it.
2. In the repo: Settings > Pages > Source: "Deploy from a branch", branch `main`, folder `/ (root)`. Save.
3. Wait a minute, then open the URL GitHub shows. Put that URL in this README and in the hub footer if you like.
4. Feedback: make a Microsoft Form with three questions (Which preview? / How useful would this be, 0 to 10? / Anything you'd change?), get its share link, and paste it into `feedback.html`. To have the preview name filled in automatically, use Forms' "Get pre-filled link" and copy the parameter name into `PREFILL_PARAM`.
