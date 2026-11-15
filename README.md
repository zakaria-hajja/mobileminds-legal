# mobileminds-legal

Privacy policies, terms of use and support pages for apps published by **Hajja Labs**, the trading
name of Zakaria Hajja, served with GitHub Pages at `https://zakaria-hajja.github.io/mobileminds-legal/`.

The pages name the publisher as "Hajja Labs, the trading name of Zakaria Hajja": Google Play requires
the privacy policy to name the developer shown in the store listing ("Hajja Labs", a personal account,
so the data controller is Zakaria Hajja). The repo and URLs keep the old `mobileminds-legal` name
because published URLs never move.

Plain static HTML: no build step, no scripts, no trackers, no external fonts. `.nojekyll` tells
GitHub Pages to serve the files as they are.

## Layout

```text
index.html               list of apps, linking to each app's pages
<app>/privacy/index.html  https://zakaria-hajja.github.io/mobileminds-legal/<app>/privacy/
<app>/terms/index.html    https://zakaria-hajja.github.io/mobileminds-legal/<app>/terms/
<app>/support/index.html  https://zakaria-hajja.github.io/mobileminds-legal/<app>/support/ (App Store support URL)
```

Apps: `munch/` (Munch: Subscription Creatures, `com.mobileminds.munch`).

These URLs are in the apps (`defaults.legal.*` in each app's `app.properties`) and in the store
listings, so **never move or rename a published page**. Change its content instead.

## Adding an app

1. Copy `munch/` to `<app>/` (lowercase, kebab-case, short; it becomes part of the URL).
2. Rewrite the pages for the new app. Don't keep Munch's text by default: the privacy policy must
   describe what **that** app actually collects, stores and sends (check its code, its Play data
   safety answers and its App Store privacy answers), and the terms must describe what it does.
3. Set the effective date on both pages.
4. Add the app to `index.html`.
5. Open each page on a phone, in light and dark mode, before publishing.

## Changing a policy

- Update the text and the effective date (top and footer) in the same commit.
- Change the page **before** the app version that changes its data handling is released, and update
  the store answers (Play data safety, App Store App Privacy) at the same time.
- Keep the old text in git history; that is the record of earlier versions.

## Publishing (one-time)

Repo settings > Pages > Deploy from a branch > `main`, folder `/ (root)`.

These pages are drafts written for the owner; they are not legal advice. Have a lawyer review them
when the business can.
