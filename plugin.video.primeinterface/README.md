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


0.2.46: Corrects low-resolution scrolling backgrounds. Separate Amazon heroshots are preferred at 1920 pixels; a full-resolution cover preview is used while the genuine backdrop is unavailable. Background metadata look-ahead is bounded to the selected title and next two titles, with existing description read-ahead preserved. Account-scoped saved metadata retains genuine backdrop URLs. Layout, navigation, login and playback implementations are unchanged.


0.2.47: Corrects hero title typography. Main-title and continuation lines can both contain several words. Colon subtitles keep the colon on the large top line; spaced dashes start the smaller subtitle. Long titles without separators wrap between words, with smaller continuation lines. Short titles stay intact. Provider spelling, the existing font, navigation, artwork selection and playback remain unchanged.


0.2.48: Restores native Kodi last-used tracking through normal video plug-in registration. The dedicated interface opens in the same invocation, with an owned artwork overlay during the directory handoff and explicit cleanup before interaction. Exit returns to Kodi Home; signed-out Back no longer opens an empty genre grid. Actual isolated Kodi 22 RC2 run confirmed native lastUsed advancement, the existing application window, overlay removal and one Back to Home. No direct writes to Kodi's shared database and no provider login or playback test. Login, catalog fetching, playback, title layout and backdrop selection remain unchanged.


0.2.49: Wide horizontal genre cards use Amazon navigation art, a visible next-card preview and an obvious white focus frame. A separate bounded preload lane warms the focused category and one neighbour. A cold selection retains its chooser until the first result is ready, then binds the existing preloaded page. Playback terminal callbacks request the original card before provider STOP reporting and cleanup, without the old one-second grace; fresh In Progress still follows the final progress attempt. Actual isolated Kodi 22 RC2 local-video run returned to the same selected card and focus in 76 ms and confirmed native horizontal genre navigation/boundary focus. This does not measure Amazon DRM/network latency or a physical display mode switch. Existing native plugin usage tracking, launch overlay, content pagination, title layout and backdrop resolution remain.


0.2.50: In Progress now follows the declared Continue Watching collection continuation and progressively publishes its fresh batches automatically, with repeated-page guards and cancellation when the section/account changes. TV containers are retained when an earlier episode is complete; active partial re-watches are retained. Provider fractional percentages, explicit position fields and playback-action resume position now reach card labels and native progress bars. Played position and remaining time are shown; percentage-derived times are marked approximate and absent values are not invented. Genre cards use the existing complete landscape stills when Amazon supplies only a category gradient, then upgrade from already preloaded actual results without opening every genre. Diagnostics report collection structure, batch completion, media counts and progress availability. Verification covers actual saved public catalog responses, actual image HTTP/decoding, all26 local tile images and deterministic time formatting; the latest private account history has not been exercised. Login/security, launch/last-used and earlier Stop-return changes remain unchanged.


0.2.51: Movie/TV genres now use one dominant cinematic image plane with oversized white genre lettering, narrow previous/next previews and vertical spine names, following the supplied references. Kodi native Focus/UnFocus transforms provide320ms collapse/expand motion. Stable native list widths plus edge transforms fill missing-neighbour space; bounds clamp and Up returns to the section selector. The list begins Action & Adventure, Anime, Comedy, Documentary; All Movies/TV remains at the end. Oversized/vertical lettering is pre-rendered from the already bundled font, with no new dependency, input-thread text drawing or network request for motion. Existing artwork and focused/next preloading remain. Extras retains its previous card panel. Actual official Kodi22RC2 UI inspection confirmed the native states, image/type binding, first/last edges, boundary focus and Up. Provider login/catalog/playback were not exercised;50 history/progress logic and49 Stop timing remain byte-identical.


0.2.52: Back exits the signed-out interface independently of catalog worker state. Expanded genre names use half-size centered title plates; thin spines and all typography image assets remain unchanged. Extras warms its directory after the main catalogs and displays each actual batch as it arrives, preserving selection by service name and retaining available cards if a later page fails. Incomplete directories are temporary account-scoped memory, never persisted as a complete list. Actual native Kodi keyboard/WindowXML checks returned to Home with real empty account storage, both before and after setting the catalog stop flag. A real public Amazon directory read published48 then102 services before a later continuation returned HTTP503; private authenticated service navigation was not exercised. User confirmed missing older In Progress titles are absent from Amazon Continue Watching too; history, login and playback protocol code is unchanged.


0.2.53: Expanded genre titles now use the same bundled font at a fixed288px on1520x700 transparent plates, displayed at144px nominal size in the existing760x350 box. Longer labels wrap at fixed line spacing, with no per-label enlargement, shrinking, cropping or glyph stretching. Native first/last edge-fill transforms apply to background/underline only; text is centered by translation. Thin-strip images and layout are unchanged. New title filenames reflect image content, fixing native Kodi reuse of old cached pixels without clearing user caches;28 obsolete title plates leave the current package. Actual native Kodi22RC2 inspection confirmed the corrected first Action & Adventure, middle Anime, and final All Movies states. An initial actual preview exposed stale textures and motivated the filename correction. All28 images share dimensions/font metrics,28 spines are byte-identical, and only the focused genre XML changes.52 exit/Extras/backend/history/login/playback behavior is preserved. Diagnostics report bundled typography measurements and observe focus/index/count during visual refresh. No private provider test or simulated provider success.
