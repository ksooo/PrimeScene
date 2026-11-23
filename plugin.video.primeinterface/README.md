# Smooth Prime

A dedicated Prime Video interface for Kodi, maintained by AgreeWithScotty.

In Progress is fetched fresh from Amazon on every visit and playback return.
Movies and TV show Prime-included titles; Sports and Purchases have separate
selectors. Catalog pages, artwork and descriptions preload independently.
Shows open their episodes and seasons; movies play their selected title.
Keyboard/remote focus starts on In Progress. Playback returns to its card.

Native account prompts handle Amazon verification without opening a browser.
Sign-out invalidates the session and purges account data before another login.
The catalog, HTTPS transport and media playback backend are independent native
implementations with no former provider fallback or runtime import.

Playback uses Kodi InputStream Adaptive/Widevine. It requests the actual selected
provider media resource and relays CDM license requests without changing sources,
decrypting content or extracting keys. Native Kodi controls remain. Local resume
storage is separate from Amazon's fresh In Progress list.

Settings contains account, playback, updates and complete diagnostics. Reports
capture release/environment, operation/attempt/request IDs, stages/timings,
redacted HTTP redirects/status, parser/protocol and provider error codes,
native player/window state, cancellation/failure and logging errors. Passwords,
verification codes, tokens, cookies and private account identities are excluded.

Same permanent add-on ID: plugin.video.primeinterface. Installations update in
place. See NOTICE.md and LICENSE for current source and asset licensing.


0.2.24 browsing: shows open season cards first, then the selected season episodes. Focusing a top content tab loads its section. Press Down on Movies or TV for genres, Enter to select, or Back to close the drawer. The far-right signed-in account action says Sign out. Focus glow follows the active skin font across the entire word.


0.2.25: original glow style restored with more width. Genre refresh preserves the verified list. Horizontal card edges retain focus; Up returns to the content tab. Actual provider page links continue browsing, with early lookahead. Fresh In Progress updates live list objects without clearing the screen; this visual continuity does not restore disk/list caching. Title typography keeps the first word large and the remaining words smaller underneath without overlap.


0.2.26: Movies and TV focus show illustrated genre grids; explicit selection opens content. Menu order is Movies, TV, In Progress, Extras. Extras groups sports and add-on subscriptions; sports may be Prime-included, subscription-based or pay-per-view. Fantasy See more discovery accepts the explicit accessible provider marker even when decorative SVG text follows its label. Single Grid collections continue through the public Amazon PaginateCollection form protocol with opaque tokens unchanged. Subsequent state follows hasMoreItems, startIndex and pagination.serviceToken; provider-declared end is logged explicitly. Existing early lookahead, card focus and all account/playback safeguards remain.


0.2.27: genre artwork is the first matching title from the real selected catalog, shared with navigation and loaded in a bounded preview queue. Extras is an individual-service directory from Amazon Browse all subscriptions, with native service branding and provider catalog URLs; it includes unsubscribed services. Native Kodi WindowXML labels use the active skin fonts, so glyph checks inspect the actual font13 character map and log its identity. Supported letters remain; punctuation, invalid text and missing glyphs receive readable fallbacks. The season chevron is native geometric artwork independent of text fonts. Bundled fonts and glow images are unchanged.


0.2.28 supersedes first-title artwork previews. The genre grid uses Amazon category-navigation covers and text overlays directly. All twelve public metadata records are seeded, then refreshed by one Categories response shared between Movies and TV. No individual genre/title page is fetched for artwork. Kodi background textures own the grid image download/cache, avoiding duplicate ImageCache requests. Startup selects Movies and its grid, with no In Progress or full-catalog request. Unrelated section warming is removed; a selected catalog still loads its first two pages and later pages early. Metadata refresh preserves native grid items. Genre graphics fill their tiles; the name appears inside the graphic only, with no duplicated label or caption below. Other agreed flows and source/player choices remain.


0.2.29: Blank categories now have category-specific empty messages, including genre names, service names and show/season context. Genuine request problems have separate contextual unavailability text and remain fully logged. Explicit native empty responses are valid results; unknown structures and sign-in/error responses remain failures. Existing cards stay visible after a later page error. Navigation, artwork, startup, services, paging, playback and account handling are preserved.


0.2.30: Restores early Movies/TV and focused-genre loading while retaining the genre grid. Separate foreground/background workers share exact in-flight requests, and queued speculative requests can be promoted on selection. Account-scoped genre first pages persist across restarts and are purged on sign-out. Cached cards bind directly; artwork and the leading title plate prepare before selection. Existing listing descriptions remain in the prepared packet. First-two-page loading, early lookahead, TV hierarchy, fresh In Progress and playback return remain unchanged. Diagnostics distinguish queue, reader, provider, cache and first-card delays. No Kodi-device latency or signed-in provider success is claimed from source checks.


0.2.31: A coordinated browsing update with a compact preview, two rows of five cards, exact black backgrounds, clear focus, and bundled public Amazon title-art pairs for all 26 genre choices. Visible artwork takes priority; leading descriptions prepare before genre selection. Fresh In Progress updates progress labels/bars in place. Native bindings are retained when confirmed on playback return, with the frozen refresh image above the live background. Back restores the genre picker. Native context actions expose full descriptions and Play from beginning without changing normal selection. Existing menu/glow assets, TV hierarchy, provider routes, first-two-page loading, early lookahead and account purge remain. Real downloaded assets, source geometry and publication bytes were checked; no device latency or live authenticated playback result is inferred. Removes 20 unreferenced historical category illustrations from the install package; previous published ZIPs retain them as history.


0.2.32: Restores the single horizontal row of larger cards and balanced hero proportions. Replaces split posters with one complete 16:9 landscape image for each of the 26 local genre choices; native keep aspect shows the full image, and one genre label sits beneath it within the tile. Old split-poster assets are removed from the package. Existing focus, progress, preload/paging, title actions, Back, account purge and playback-return fixes remain. Source, actual image dimensions and archive checks do not establish a remote Kodi UI outcome.


0.2.33: Personal tabs now own their screen immediately, with baked headings and multi-line guidance instead of blank or previous-section content. In Progress and Purchases dispatch directly to reserved workers; fresh history remains uncached. Personal JSON extraction avoids unrelated HTML card parsing and records stage timing. Purchases discovers nested library links/explicit library payloads and distinguishes confirmed empty media from read/auth/provider failures. Search has its own landing instructions, full Prime Video catalog description, proper result focus and Back behavior. Single-row browsing, complete genre artwork, paging, account purge and playback behavior remain. Source, real saved response extraction and actual download checks do not establish signed-in library state or device latency.


0.2.34: Navigation/lifecycle audit repairs old-card leakage on uncached views, service Back/retry, first-card restoration, stale title actions and season context. Explicit title actions have an independent worker/reader from background metadata. Temporary next-page failures retain the exact continuation and retry with bounded backoff; metadata/artwork errors can recover. Saved continuations import atomically after validation, queued playback carries an account epoch guard, Search follows the existing provider-declared Grid protocol, and actual sign-in forms have distinct messages. The single-row/genre/top-menu layouts, artwork/fonts, fresh In Progress policy and provider playback choices remain. Source, saved real-response and release artifact verification do not claim authenticated account or device-runtime success.


0.2.44: Complete user-requested restoration of0.2.34, including its original assets and menu data. Every non-release-metadata package member is byte-identical to the verified original0.2.34 ZIP. Only version/news/changelog/README differ so Kodi accepts this as release0.2.44. Restart Kodi after updating.


0.2.45: Repairs the focus/navigation regression identified in real 0.2.44 logs and the local manifest HEAD path implicated in Stop timeouts. This is a targeted patch of the restored 0.2.34 runtime. Login, dependency versions, security changes and artwork remain unchanged. Kodi add-on last-used ordering is still under investigation.
