# Privacy Policy — Bookmark Canvas

**Last updated:** July 20, 2026

This policy describes exactly what Bookmark Canvas does with your
data. It's written to match the extension's actual code, not a
generic template — if the extension changes, this document needs to
change with it.

## The short version

Bookmark Canvas does not have a server. There is no account, no
login, and no analytics. Everything it stores lives in your own
browser, on your own device, and is deleted the moment you uninstall
the extension. The only things that ever leave your device are: (1)
direct requests to websites you've bookmarked, to fetch a preview
image, and (2) a request to Google Fonts to load a typeface. Neither
of those goes through us — there is no "us" the data passes through
at all.

## What the extension can access, and why

Bookmark Canvas requests broad site access (`<all_urls>`) and access
to your bookmarks. Both are used exclusively for the extension's
core purpose: showing a visual thumbnail for each of your bookmarks.
Specifically:

- **Your bookmarks** (`bookmarks` permission) — read to display them,
  and written to when you use the extension's own features (creating
  a bookmark via right-click, moving one between folders, renaming or
  deleting a folder, etc.). The extension never reads or modifies
  bookmarks for any purpose beyond what you directly asked it to do
  through its own UI.
- **Site access** (`host_permissions: <all_urls>`) — used for two
  things, both entirely on-device:
  1. Capturing a screenshot of a page you're actively viewing, when
     you use "Bookmark this page (with screenshot)" or the extension's
     automatic background capture.
  2. Fetching a bookmarked page's own HTML to look for a preview
     image it already publishes (an `og:image` meta tag) — the same
     kind of image a site would show if you shared its link on social
     media. This is a direct browser request to that site, not a
     request that passes through any server operated by this
     extension.

## Where your data is stored

Everything the extension keeps — your captured screenshots, cached
preview images, folder colors, sort/theme/layout preferences — is
stored using Chrome's local, on-device storage (`chrome.storage.local`).
None of it is synced to a server, none of it is accessible to any
other extension or website, and none of it survives uninstalling the
extension.

Your bookmarks themselves are stored by Chrome's own built-in
bookmarks system, exactly as they would be without this extension
installed. If you have Chrome's own sync turned on, your bookmarks
sync the way they always have — that's Chrome's behavior, not
something this extension adds or changes.

## What leaves your device

- **Websites you bookmark.** When the extension looks for a preview
  image, it makes a direct request to that website — the same as if
  you'd typed the URL into your address bar. That website sees this
  request the same way it would see any visit from your browser.
  Nothing about this request is different because of the extension,
  and no third party sits between you and that website.
- **Google Fonts.** The extension's interface uses the Roboto font,
  loaded from Google's font hosting (`fonts.googleapis.com`,
  `fonts.gstatic.com`). This is a standard, widely-used font CDN —
  loading it works the same way as any website that uses Google
  Fonts, and is subject to Google's own privacy policy for that
  service.

Nothing else leaves your device. There is no analytics, no tracking
pixel, no crash reporting, and no telemetry of any kind.

## What we don't do

- We don't have a server, so we don't collect, store, or have access
  to any of your data ourselves.
- We don't sell or share data, because we don't have any to sell or
  share.
- We don't track your browsing history or behavior.
- We don't use your data for advertising.
- We don't require an account or any personal information to use the
  extension.

## Your controls

- **Uninstalling the extension** deletes everything it stored —
  screenshots, cached previews, preferences — immediately and
  completely. Your actual bookmarks remain, exactly as they were,
  since those belong to Chrome's own bookmark system, not the
  extension.
- **Removing a bookmark or folder** through the extension removes it
  from Chrome's bookmarks the same as doing so through Chrome's own
  bookmark manager would.

## Changes to this policy

If what the extension does with data changes in a future update,
this document will be updated to match, with the "Last updated" date
above reflecting the most recent change.

## Contact

Questions about this policy or the extension can be sent to:
BookmarkCanvas.dev@gmail.com
