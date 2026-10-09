# Privacy Policy — Bookmark Canvas

**Last updated:** October 8, 2026

This policy describes exactly what Bookmark Canvas does with your
data. It's written to match the extension's actual code, not a
generic template — if the extension changes, this document needs to
change with it.

## The short version

Bookmark Canvas does not have a server. There is no account, no
login, and no analytics. Everything it stores lives in your own
browser, on your own device, and is deleted when you uninstall the
extension (apart from a trial-start timestamp, explained below). The
only things that ever leave your device are: (1)
direct requests to websites you've bookmarked, to fetch a preview
image, (2) a request to Google Fonts to load a typeface, and (3)
your license key, sent to Gumroad to verify a purchase when you
activate the extension. None of those goes through us — there is no
"us" the data passes through at all.

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
preview images, folder colors, sort/theme/layout preferences, the
times you last opened or visited your bookmarked pages (see "Last
opened and visited times" below), and your license activation
status — is stored using Chrome's local,
on-device storage (`chrome.storage.local`). None of it is synced to
a server, none of it is accessible to any other extension or
website, and none of it survives uninstalling the extension, with
one exception described next.

**Trial start date.** To run the 7-day free trial, the extension
saves a single timestamp (the day you first used it) in Chrome's sync
storage (`chrome.storage.sync`), so reinstalling doesn't restart the
trial. If Chrome sync is on, Chrome syncs it through your Google
account like other synced extension data. It's the only thing the
extension stores this way, and it isn't sent to us.

Your bookmarks themselves are stored by Chrome's own built-in
bookmarks system, exactly as they would be without this extension
installed. If you have Chrome's own sync turned on, your bookmarks
sync the way they always have — that's Chrome's behavior, not
something this extension adds or changes.

## Last opened and visited times (the "Rediscover" feature)

"Rediscover" shows you bookmarks you haven't used in a while. To know
which ones those are, the extension remembers when you last used each
bookmark:

- **When you open a bookmark from the extension's canvas.**
- **When you view a page that is one of your bookmarks** (for
  example by typing its address or following a link). The extension
  records the time for that page **only if it is currently
  bookmarked**. Visits to pages that are not bookmarks are not
  recorded, and no list of other sites you visit is kept.
- **Chrome's own "last used" time for a bookmark**, which the
  extension reads from Chrome's bookmarks system when your version of
  Chrome provides it.

Only a timestamp per bookmarked page is kept (no page content, no
history of repeated visits). It is stored on your device in
`chrome.storage.local`, is never sent anywhere, and is deleted when
you remove the bookmark or uninstall the extension. The extension's
own background thumbnail refreshes do not count as visits.

## Backup files (Export / Import)

The "Backup Thumbnails" button (bottom-left of the extension) lets you
save your bookmarks and thumbnails to a file and load them on another
device. Exporting is also offered on the screen shown when the free
trial ends, so your data is yours to keep whether or not you buy. A
backup file is created only when you choose "Export backup" from that
menu (or "Export my thumbnails" on the trial-ended screen), and it is
saved by your browser to wherever you choose, like any download.

It contains: your bookmarks (their titles, web addresses, folders and
order), their thumbnails, the last-opened/visited times described
above, folder colors, and pinned positions. Only web links (http and
https) are included; other kinds, such as bookmarklets, are left out.
Nothing is uploaded: the file goes only where you put it, and the
extension never sends it anywhere. Because it contains your bookmark
titles and links, treat it as you would any private file.

"Import backup" reads a file you pick and first shows you a summary:
how many bookmarks and folders would be added, how many are already on
the device, and how many thumbnails are new, would replace older ones,
or are kept because you already have newer ones. Only after you
confirm does it add the missing folders and bookmarks (using Chrome's
bookmarks permission) and the thumbnails and settings. It never deletes
or moves anything you already have, skips web addresses you have
already bookmarked, and ignores anything in the file that is not a
plain web link.

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
- **Your license key, when you activate the extension.** Bookmark
  Canvas requires a one-time purchase, handled entirely by Gumroad.
  When you enter your license key, it's sent directly to Gumroad's
  verification API (`api.gumroad.com`) to confirm it's valid and see
  which tier (Standard or Standard + Positioning) it unlocks. No other information — no
  bookmarks, browsing activity, or personal details — is sent along
  with it. The result (which tier you own) is then stored locally on
  your device the same way everything else is. Gumroad's handling of
  your purchase and license key is governed by
  [Gumroad's own privacy policy](https://gumroad.com/privacy),
  since that transaction happens on their platform, not ours.

Nothing else leaves your device. There is no analytics, no tracking
pixel, no crash reporting, and no telemetry of any kind.

## What we don't do

- We don't have a server, so we don't collect, store, or have access
  to any of your data ourselves.
- We don't sell or share data, because we don't have any to sell or
  share.
- We don't build a browsing history. The only visit information kept
  is the last-visited time of pages you have bookmarked, described
  above, and it never leaves your device.
- We don't use your data for advertising.
- We don't require an account to use the extension. Purchasing does
  require going through Gumroad's checkout, which is between you and
  Gumroad — we never see your payment details, name, or email; we
  only ever see whether a license key you enter is valid.

## Your controls

- **Uninstalling the extension** deletes everything it stored on your
  device — screenshots, cached previews, preferences, and license
  activation status — immediately and completely, except the
  trial-start timestamp described above, which Chrome manages through
  sync. Your actual bookmarks remain,
  exactly as they were, since those belong to Chrome's own bookmark
  system, not the extension.
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
