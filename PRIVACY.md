# Smart Trader – privacy policy

Effective since 2026-10-10, for the browser extension. The same text in three languages: [English](#english) · [Українська](#українська) · [Русский](#русский).

---

## English

**Effective date:** 2026-10-10 · **Contact:** ggggggdev@gmail.com

Smart Trader adds trading tools to Steam pages: trade offer summaries and item prices, faster accepting of the offers
you choose, inventory and Community Market helpers, trade history summaries, partner reputation checks, phishing and
scam warnings and desktop alerts. This policy describes every piece of data the extension handles, where it goes and
how to delete it. It matches the extension's code; if the code changes what it does with data, this policy and the
in-extension notice change with it, and the extension asks for your agreement again before doing anything.

### 1. Nothing happens before you agree
After installation the extension shows a data notice. Until you press "I agree", it does nothing on Steam pages: it
reads no page data, stores nothing and makes no requests.

### 2. Data kept on your computer
Stored in your browser's extension storage (`chrome.storage.local`) on this computer, never sent to us or anyone:
- your Smart Trader settings and the state of its panels and tours;
- item marks and the notes the tools keep about items;
- trade links you save (they contain the partner's trade link token and, once read, the partner's nickname and avatar
  address) and your own trade link (with your nickname and avatar address);
- summaries and caches built from pages you opened: trade and inventory history summaries, item descriptions,
  Community Market prices, partner reputation results, friends lists, records of offers you accepted (with the
  partner's nickname), the store cart history;
- your own nickname per account (a day), so that a desktop notification can carry it as its title; the items of the
  trade offers you sent from this browser (names and pictures; 60 offers per account, 5 accounts, 15 days at most), so
  that the notification of such an offer's acceptance can name them;
- the listings you put up for sale that still wait for your confirmation (the Steam Mobile app or e-mail), so that
  the selling tools never list those items again; each is kept for a week at most;
- what the card set tools read from your own Steam badges: the sizes and card lists of the badges' card sets, your own
  badge levels and how many copies of each card you own (kept with a one-way hash of your account, so another account
  signed in on this browser never sees them), and your account level and XP; another profile's badge levels are kept
  only while its page is open, never stored;
- the choices you made in the extension's options (optional services, sound);
- your pricempire API key, if you enter one in Smart Trader's settings: kept apart from the settings, sent only to
  pricempire (section 5), never shown on another site's page;
- (since 1.12.0) what the Phishing and scam protection (its own tab in Smart Trader's settings, on by default) needs to
  notice a change, as one-way keyed hashes only (fingerprints made on this computer with a random key of this
  installation; the data cannot be read back from them): the sessions and devices of your account's authorized devices
  list and your account's e-mail, phone and Steam Guard lines; the trade offers sent from this browser (15 days at
  most); the offers you cancel on Steam's offers pages (15 days at most, so that a cancel of your own is never taken
  for a phishing sign); the sessions, offers and chat partners you marked with "Yes, it was me" or "Different person"; the sessions
  and offers an alert was already raised for (so that it is not raised again at every check: a device alert closed
  with × comes back a day later while it is still true); besides them, the times of its automatic cancel tries (for
  the limit of 5 an hour), how many items your own inventory has on Steam's server per game (counts only, no item), when
  the check of your offers started for your account, the keyed hash of the partner of an offer this browser is sending
  (10 minutes), your own offers cancelled elsewhere (as hashes, 40 minutes), the cancels still queued and which tab leads
  a check. The words of an open security alert (a device's name and place, a trade partner's SteamID and nickname, the
  ids of the offers it is about) are kept only in that alert, until you answer or close it, for 24 hours at most; a chat
  impostor alert keeps as its words the two nicknames it compared and the chat partner's SteamID, the same way. With
  the Trade offers tab off, the protection keeps the background offer watch running for its trade check, with that
  watch's usual records: your account's SteamID with its offer counts, and the ids of the accepted sent offers it has
  read. The web chat's friends list and its open one-to-one chats (names, the names you gave your friends, avatars; group chats
  never) are read on your computer while the chat page is open and are not stored beyond the words of an open alert
  (above). Your Incoming and Sent offers pages,
  read for the hidden sent offers check (since 1.12.1) and the trade items check (since 1.12.2: the items of each offer),
  are compared with what the page shows in memory and not stored (their offers, partners, items and item games are not
  kept; only an alert one of the checks raises keeps, as its words, the ids of the offers it is about — 10 at most — and,
  for a hidden offer not sent from this browser, its partner's SteamID and nickname, until you answer or close it, 24
  hours at most). None of it is sent anywhere;
- (since 1.12.1) the value of your own inventories shown next to the wallet balance, per account (three at most): the
  price source, the totals, the item counts and when — never an item, a name or a list, kept under the account's
  SteamID;
- your answer to the data notice and your acceptance of the License Agreement: only its version, the time and your
  choice about automation (auto accept, auto-cancel), with no account data.

A few page features also keep small values in the Steam site's own storage in your browser (`localStorage` and
IndexedDB of steamcommunity.com or store.steampowered.com, for example the market price caches of the selling tools,
and the price lists of the price sources you turned on: item names with their prices and counts, nothing about you;
since 1.12.1, while a blur for streams is on, which of the three is on — the wallet, names, avatars — so that it holds
from a page's first frame), as Steam's pages do themselves.

### 3. Your Steam session and tokens
While you use Steam pages, the extension's page code uses the session id and the web token that the open Steam page
itself holds, and the trade link tokens of trade links. They are used **only** in requests to Steam
(`steamcommunity.com`, `store.steampowered.com`, `checkout.steampowered.com`, `api.steampowered.com`), exactly as the
Steam page would use them. The session id and the web token are never stored by the extension and never passed to its
background part. Trade link tokens are stored only inside the trade links you keep (section 2). None of them is ever
sent anywhere else: the extension's background part refuses any request to a host that is not Steam's that looks like
it carries one.

### 4. Requests to Steam
The tools read the Steam pages you open and ask Steam for more of the same (more history, item descriptions, prices,
offer states) with your Steam session, as the page would. The card set tools read your own badges' details from Steam
(the card sets, your levels and XP), and a public profile's badge pages only when you ask for that profile's levels.
Crafting badges from card sets is a change on your account: it is sent to Steam (one craft at a time) only after you
have seen the plan — the games, the sets and the XP — and confirmed it; it can be stopped at any time. The other
changes on your account are sent to Steam only when you start them: accepting the offers you choose, putting items up
for sale on the Community Market (after the review of the prices, or — when you choose "Sell as prices come in" after
its warning — each item as soon as its price has been read) or taking listings down, turning items into gems and
opening booster packs. The first exception is auto accept (off by default): after your separate consent (its own box,
"Allow automatic acceptance of incoming gift trade offers", unticked until you tick it) and once you turn it on, it accepts, on its own, incoming offers in which you give nothing. The
second exception is the auto-cancel of the Phishing and scam protection (since 1.12.0, "Off" by default): it needs the
same consent to automation (without it the setting reads "Off"), and once you choose "Only on phishing signs" or "All
not sent from this browser" it cancels, on its own, trade offers sent from your account but not from this browser —
one request to Steam per offer, at most 5 tries an hour (a try that fails counts too); an offer sent from this browser
is never cancelled, nor (since 1.12.1) one already on trade hold or under Steam's trade protection (everything you give
in it a Counter-Strike 2 item) while "Do not auto-cancel offers already on trade hold (escrow) or under trade
protection" is on (on by default). The protection's checks only read, with your Steam session: your account's authorized devices list
(`api.steampowered.com`, with the page's web token, every 20 minutes by default, from one tab) and, every third time,
the Security & Devices page (`store.steampowered.com/account/authorizeddevices`) for the e-mail, phone and Steam Guard
lines (read from an open `store.steampowered.com` tab; while none is open, these lines wait); your sent offers, with
the background offer watch's own requests (its counts; its sent list when those counts move and at most every 5
minutes while one of your sent offers is waiting — with the Trade offers tab or its notification of accepted offers
off, these list reads are made for this check; for an alert about such an offer, one read of its partner's public
Steam profile — and, on a phishing sign, of the cancelled offer's partner — for the nickname the alert shows); your own
inventory from Steam's server, to compare with what the inventory page shows — when you open your
inventory (at most once every 6 hours by default; about one request per game and item category) and, in between, its
totals alone from one tab; (since 1.12.1) your own sent offers page (`steamcommunity.com/…/tradeoffers/sent/`, the address you have open),
when you open it or the window of an offer you sent — at most one request a minute from one tab, its answer used for 5
minutes —, only to compare it with
what the page shows (an offer that something in your browser hides); (since 1.12.2) your own incoming offers page
(`steamcommunity.com/…/tradeoffers/`) the same way, when you open it or the window of one of your offers, and once for a
gift waiting for auto accept (at most one request every 10 seconds), only to compare the items each offer shows with
Steam's own record of it (items painted into an offer or hidden from it). The web chat's friends and dialogs are read in
the chat page itself, with no request to Steam's servers apart from loading the avatar pictures of look-alike pairs
from Steam's picture servers (avatars.fastly.steamstatic.com or the chat page's own avatar host), as the page loads them, without cookies or referrer. The
background part asks Steam's public store API (`store.steampowered.com/api/appdetails`, `/api/packagedetails`) for
prices and pictures of games and packages without your cookies, and, for the inventory check only, reads your own
inventory (`steamcommunity.com/inventory/…`, nothing else) with your Steam cookies, so that no script of the page can
see or change the answer: the browser adds the cookies itself; the background part neither reads nor keeps them,
follows no redirect and sends them to no other address. The extension's background part also reads your sent trade
offers page (since 1.12.1) and your incoming trade offers page (since 1.12.2) on steamcommunity.com (those two
addresses, no other), the same way, only to compare them with what the page shows; nothing is stored. (Since 1.12.1)
The inventory value next to the wallet balance reads your own inventories (TF2, CS2, Dota 2, Steam; Rust when your
price source prices it) from Steam with the page's own requests, from one tab, on a click on Σ or, set to
"Automatic", by itself every 30 minutes, never while a trade is being accepted or sent. Item pictures come from
Steam's image servers.

### 5. Optional services
The three reputation sites are turned on only by you: on the page shown before Smart Trader starts (their box there is
unticked until you tick it; the browser asks you to allow the sites) or later in the extension's options. So are the
price sources (since 2026-10-09): marketdb.info, pricempire and the marketplaces' public price files (Market.CSGO and
its TF2, Dota 2 and Rust sites, Waxpeer, LOOT.FARM, Lis-Skins), each with its own box on that page (unticked until you
tick it) or later in the options; Smart Trader asks one only while it is the price source in its settings
(marketdb.info also while a marketplace is: its exchange rates convert their US dollar prices, and its price lists value
the items the marketplace does not price when "Items the marketplace does not price" is set to "marketdb.info after
Steam's fee and the cash-out fee"). marketdb.info is Smart Trader's default price source (since 1.12.2): until you turn it on, Smart Trader
takes its prices from the Steam Market instead. They receive nothing
about you or your items: the game, the time window or the marketplace of a whole price list, and pricempire also your
own API key. pricempire works only with your own key from your pricempire account: you enter it in Smart Trader's
settings, it is kept in the extension's storage on this computer apart from the settings, and it is sent only to
`api.pricempire.com`, as the `Authorization` header of its requests, never in an address and never to any other host
(the extension's background part forwards it there only and keeps no copy); it is never shown on another site's page
and never written to the diagnostic log. The keys.land price relay is allowed from the start (its host is installed with the
extension), and Smart Trader asks it only while its prices are on in Smart Trader's settings (KEYS.LAND → "Use
KEYS.LAND prices", on from the start since 1.12.2; the KEYS.LAND tab's switch turns it off; since 1.12.4 the one switch
of those prices with any price source, a marketplace included), or, for its Steam conversion figures only, while a
marketplace is the price source and the items it does not price are valued less the automatic cash-out fee, or while
Steam Market or marketdb.info prices are shown as cash ("Cash after the cash-out fee", on by default; always while
KEYS.LAND is on); it receives nothing about you. You can turn any of them off in the options at any
time. None of them receives cookies from the extension, except SteamTrades: the SteamTrades request carries your own
steamtrades.com cookies, so the site answers as it would in your own tab (it is needed to pass its bot check); this
happens only while SteamTrades is turned on, only on that one request, and the form tokens of its page are removed from
the answer before Smart Trader reads it. Each of them,
like any website, sees your IP address, your browser's name and version (User-Agent) and the time of the request.

| Service | What is sent | When |
| --- | --- | --- |
| keys.land price relay (the host listed in the extension's permissions) | only which price is wanted: `GET …/kl/v1/market/series?item=key` (or `ticket`, `gems`) `&range=24h`; and the Steam conversion figures of keys, tickets and gems: `GET …/kl/v1/steam/convert` (no parameter). Nothing about you or your account. | when prices of TF2 keys, tickets or gems are shown (at most once a minute) — only while KEYS.LAND prices are on in Smart Trader's settings (on from the start since 1.12.2; the KEYS.LAND tab's switch turns them off; with any price source, a marketplace included); the conversion figures only while a marketplace is the price source and the items it does not price are valued less the automatic cash-out fee, or while Steam Market or marketdb.info prices are shown as cash (on by default; always while KEYS.LAND is on) (at most every few minutes); the relay itself is allowed from the start and the options can turn it off |
| backpack.tf (`backpack.tf`) | the public SteamID64 of the profile or trade partner you look at: `GET https://backpack.tf/api/IGetUsers/v3?steamid=<SteamID64>` | when you open a profile, a trade offer or the trade history |
| SteamTrades (`www.steamtrades.com`) | the same SteamID64: `GET https://www.steamtrades.com/user/<SteamID64>`, with your own steamtrades.com cookies (since 2026-10-07; needed to pass its bot check) | the same |
| CSGO-Rep (`api.csgo-rep.com`) | the same SteamID64: `POST https://api.csgo-rep.com` with `{"id": <number>, "query": {"steam_id": "<SteamID64>"}}`; now and then `GET https://api.csgo-rep.com/config` (nothing about you) | the same |
| marketdb.info (`marketdb.info`) | only the game id and the time window of a whole price list: `GET https://marketdb.info/api/v1/prices?game=<game id>&hours=<24, 168 or 720>`; once a day the exchange rates: `GET https://marketdb.info/api/v1/exchange-rates`. Nothing about you or your items, never an item's name. | when prices of a game are shown and its kept list is older than a few hours — only while the service is on and marketdb.info is the price source, or a marketplace is (its exchange rates, and its price lists when "marketdb.info after Steam's fee and the cash-out fee" values the items the marketplace does not price) |
| pricempire (`api.pricempire.com`) | the game id, the marketplace and your own API key: `GET https://api.pricempire.com/v4/trader/items/prices?app_id=<game id>&sources=<marketplace>&currency=USD` (with a subscription `/v4/paid/…`), with the header `Authorization: Bearer <your key>`; now and then `GET https://api.pricempire.com/v4/free/status` (or `/limits`, `/currencies`) with the same header. Nothing else about you or your items. | when CS2 prices are shown and the kept list is older than its refresh time — only while pricempire is the price source and the service is on |
| marketplace price files (`market.csgo.com`, `tf2.tm`, `market.dota2.net`, `rust.tm`, `api.waxpeer.com`, `loot.farm`, `lis-skins.com`) | only the request for the public price file of a game, for example `GET https://market.csgo.com/api/v2/prices/USD.json`, `GET https://api.waxpeer.com/v1/prices?game=csgo&minified=1`, `GET https://loot.farm/fullprice.json`, `GET https://lis-skins.com/market_export_json/csgo.json`. Nothing about you or your items, no key. | when prices of a game are shown and the kept list is older than two hours — only from the marketplace chosen as the price source, and only while the service is on |

Results are kept on your computer for a few hours (section 2); the price sources' lists only as item names with
their prices and counts. The keys.land price relay is run by the author of Smart
Trader; it only forwards public price data from KEYS.LAND, an independent service whose data is used with its owner's
permission. The relay keeps only ordinary server logs (the requested address and the time) for a short time and nothing
about your account. backpack.tf, SteamTrades, CSGO-Rep, marketdb.info, pricempire and the marketplaces each apply
their own terms and privacy policy, published on their sites.

When you turn backpack.tf on, the extension also runs its tools on the backpack.tf pages you open (listing prices in
trade offer links, backpack totals); before that it does not run there at all. On those pages only your settings, the
state of the tips and the values of the backpack.tf tools themselves are made available to the page; your saved trade
links, trade partners, offer records, reputation results, purchase history and the diagnostic log are not.

Unusual effect pictures (Smart Trader's settings → Items & inventory, off by default): when you turn them on, the
browser loads those pictures from itempedia.tf (`https://itempedia.tf/assets/particles/<effect number>_94x94.png`). Like any
picture server, it sees your IP address, your browser and the time; nothing else is sent.

3D view of CS2 items (Smart Trader's settings → Items & inventory, on by default): nothing is sent until you click
3D. Your click opens a new tab on the viewer you chose (skinflow.gg by default; csmarketcap.com or swap.gg from the ▾
menu) with only the item's inspect link in the address — the same link Steam shows behind "Inspect in Game…". The first
time, Smart Trader asks you before it opens (you can turn that question off). Since 2026 that link encodes the item
itself: type, finish, pattern seed, wear (float), stickers and charms with their positions and wear, a StatTrak™ count,
a name tag's text and the asset id, and it may carry the owner's account number; an older link instead holds the
owner's SteamID64 (or the market listing id), the asset id and a check number. No cookies, Steam session, token or
trade link go with it; the tab opens without a referrer. The viewer sees your IP address, browser and time, and may
pass the link on to its own services (for example, its 3D renderer); its own terms and privacy policy apply. The Details panel decodes the link on your computer and sends nothing.

Links to other sites (for example SteamDB, backpack.tf, SteamTrades, Steam Card Exchange) are ordinary links: those
sites receive nothing unless you open the link.

### 6. Diagnostic log
The diagnostic log (`dev.log`) is off unless you turn it on (Smart Trader's settings on a Steam page → General →
Diagnostics). While it is on, it keeps on your computer only what is needed to find faults and slowness: timings,
counts, error messages (scrubbed) and the status of network requests, for at most 7 days and 4 MB. The file you
download also names your browser and its version, operating system, screen size class and pixel density, interface language and time
zone offset, the extension or script engine that runs it and its version, Smart Trader's versions on this installation
and when it was first installed, your settings as set (text settings by key only, never their value), the state of its
tips and a random code of this installation that tells its logs apart from another installation's. It never records
profiles: no SteamIDs, names, avatars, profile or trade links, tokens, session ids or page addresses; ids of offers and
trades only as salted one-way hashes. It leaves your computer only if you download it ("Download log") and send the
file yourself; "Clear log" deletes it.

### 7. What the extension does not do
- No analytics, no tracking, no ads, no affiliate links.
- No selling, renting or sharing of your data with anyone, including advertising platforms, data brokers and
  information resellers; no use for credit-worthiness or lending.
- No human reads your data: we (the developers) never receive it.
- No remote code: all of the extension's code is in its package; answers from the internet are used only as data.
- All requests use HTTPS.

**Limited Use.** Smart Trader's use of user data complies with the Chrome Web Store User Data Policy, including the
Limited Use requirements.

### 8. Keeping and deleting data
Data stays on your computer until you delete it. The extension's options have "Delete all Smart Trader data", which
removes everything in section 2 that lives in the extension's storage (but your answer to the data notice and your
acceptance of the License Agreement) and gives
the optional services' site access back to the browser. Removing the extension removes its storage as
well. Values kept in the Steam site's own storage (section 2) stay until you clear that site's data in the browser.
Caches expire and are trimmed on their own.

### 9. Changes
When what the extension does with data changes, this policy is updated, the date above changes, and the extension
shows its data notice again and waits for your agreement before doing anything.

Changes: 2026-10-07 — the SteamTrades request carries your own steamtrades.com cookies (section 5), only while
SteamTrades is turned on. 2026-10-09 — the optional price sources marketdb.info, pricempire (with your own API key)
and the marketplaces' public price files (sections 2 and 5), each off until you turn it on; the keys.land relay also
gives the Steam conversion figures. 2026-10-09 (1.12.0) — the Phishing and scam protection (sections 2 and 4): the
authorized devices list and the e-mail, phone and Steam Guard lines read from Steam and kept only as one-way hashes,
your own inventory read from Steam's server for the tamper check (by the background part, with your Steam cookies), the web chat's friends and one-to-one chats read on
your computer, and the optional auto-cancel of trade offers not sent from this browser (off by default; it needs the
consent to automation). 2026-10-10 (1.12.1) — the hidden sent offers check (sections 2 and 4): your own sent offers
page, read by the background part with your Steam cookies only to compare it with what the page shows, nothing stored
(the same data the offer watch already reads, so no new notice); auto-cancel never cancels an offer already on trade hold or
under Steam's trade protection (everything given in it a Counter-Strike 2 item) while its new safety setting is on (on
by default); an alert of hidden offers keeps their ids as its words (section 2); the inventory value next to the
wallet balance, kept as totals only (sections 2 and 4); while a blur for streams is on, which of its three switches is
on, in the Steam site's own storage (section 2). 2026-10-10 (1.12.2) — the trade items check (sections 2 and 4): your
own incoming offers page too, read by the background part with your Steam cookies only to compare the items each offer
shows with Steam's own record of it, nothing of it stored but an alert's offer ids (section 2) (the same data the offer
watch and auto accept already read); KEYS.LAND prices on from the start and marketdb.info as Smart Trader's default
price source (section 5): this update turns KEYS.LAND on once for every installation (the KEYS.LAND tab's switch turns
it off again), shows Steam Market and marketdb.info prices as cash by default (the keys.land relay's Steam conversion
figures — the same request as before, now also for this) and makes marketdb.info the default source (it is still asked
only after you turn it on here; until then the prices come from the Steam Market); the 3D view of CS2 items (section
5): a viewer opens in a new tab only on your click, with the item's inspect link in its address; nothing is sent before
that click. Because KEYS.LAND and the cash view turn on for existing installations too, the extension
shows its data notice again (its version 10). This version of the policy also names what earlier versions left out: in
section 2 your own nickname, the items of the offers you sent, the saved trade links' nicknames and avatars, the
partner's nickname in the records of accepted offers, the foreign-trade check's working records, a chat impostor
alert's words and the inventory value kept under your account's SteamID; in section 4 the one read of a partner's
public profile for an alert's nickname and the avatar pictures of look-alike chat pairs; in section 6 everything the
diagnostic log's file holds. 2026-10-10 (1.12.4) — the price providers follow one table (section 5): "Use KEYS.LAND
prices" is the one switch of those prices with any price source (the marketplaces' "Keys, tickets and gems at the
KEYS.LAND cash price" is that switch now), and Steam Market or marketdb.info prices can be shown as the market price,
as cash or as the Steam balance received; the keys.land relay's conversion figures are asked whenever they are shown as
cash, KEYS.LAND on or off — the same anonymous request as before, never for the market price or the Steam balance.

### 10. Contact
ggggggdev@gmail.com

Smart Trader is an independent project. It is not affiliated with, endorsed or sponsored by Valve Corporation. Steam
and the Steam logo are trademarks and/or registered trademarks of Valve Corporation in the U.S. and/or other countries.

---

## Українська

**Діє з:** 2026-10-10 · **Контакт:** ggggggdev@gmail.com

Smart Trader додає інструменти для обміну на сторінки Steam: зведення пропозицій обміну й ціни предметів, швидше
прийняття вибраних вами пропозицій, помічники для інвентарю й торговельного майданчика, підсумки історії обмінів,
перевірку репутації партнерів, попередження про фішинг і скам і сповіщення на робочому столі. Ця політика описує
всі дані, з якими працює розширення, куди вони йдуть і як їх видалити. Вона відповідає коду розширення; якщо код
почне інакше поводитися з даними, зміниться і ця політика, і повідомлення в розширенні, а розширення знову попросить
вашої згоди, перш ніж щось робити.

### 1. Нічого не відбувається без вашої згоди
Після встановлення розширення показує повідомлення про дані. Доки ви не натиснете «Погоджуюсь», воно нічого не
робить на сторінках Steam: не читає даних сторінок, нічого не зберігає й не робить запитів.

### 2. Дані на вашому комп’ютері
Зберігаються в сховищі розширення вашого браузера (`chrome.storage.local`) на цьому комп’ютері й нікому не
надсилаються, зокрема й нам:
- ваші налаштування Smart Trader і стан його панелей і турів;
- мітки предметів і нотатки, які інструменти ведуть про предмети;
- збережені вами посилання для обміну (вони містять токен посилання партнера, а після прочитання — нікнейм партнера й
  адресу його аватара) і ваше власне посилання (з вашим нікнеймом і адресою аватара);
- підсумки й кеші з відкритих вами сторінок: підсумки історії обмінів та інвентарю, описи предметів, ціни
  торговельного майданчика, результати перевірки репутації, списки друзів, записи прийнятих вами пропозицій (з нікнеймом
  партнера), історія кошика магазину;
- ваш власний нікнейм для кожного акаунта (добу), щоб сповіщення на робочому столі могло бути підписане ним; предмети
  трейдів, надісланих з цього браузера (назви й зображення; 60 трейдів на акаунт, 5 акаунтів, не довше 15 днів), щоб
  сповіщення про прийняття такого трейду могло їх назвати;
- ваші лоти, які ще чекають вашого підтвердження (у мобільному застосунку Steam чи поштою), щоб інструменти продажу
  ніколи не виставляли ці предмети знову; кожен зберігається не довше тижня;
- те, що інструменти наборів карток читають із ваших власних значків Steam: розміри й списки карток наборів, ваші
  рівні значків і скільки копій кожної картки у вас є (зберігаються з одностороннім хешем вашого акаунта, тож інший
  акаунт, що входить у цьому браузері, їх не бачить), а також рівень і XP вашого акаунта; рівні значків чужого профілю
  тримаються лише поки відкрита його сторінка й не зберігаються;
- ваш вибір у параметрах розширення (додаткові сервіси, звук);
- ваш API-ключ pricempire, якщо ви введете його в налаштуваннях Smart Trader: зберігається окремо від налаштувань,
  надсилається лише до pricempire (розділ 5) і ніколи не показується на сторінці іншого сайту;
- (з 1.12.0) те, що потрібно Захисту від фішингу та скаму (окрема вкладка в налаштуваннях Smart Trader, типово
  ввімкнена), щоб помітити зміну, — лише як односторонні ключовані хеші (відбитки, зроблені на цьому комп’ютері з
  випадковим ключем цього встановлення; самих даних з них не прочитати): сесії й пристрої зі списку авторизованих
  пристроїв вашого акаунта і рядки e-mail, телефону й Steam Guard вашого акаунта; трейди, надіслані з цього браузера
  (не довше 15 днів); трейди, які ви скасовуєте на сторінках трейдів Steam (не довше 15 днів, щоб власне скасування
  ніколи не сприймалося як ознака фішингу); сесії, трейди й співрозмовники, яких ви позначили «Так, це я» чи «Це інша людина»; сесії й
  трейди, про які вже була тривога (щоб вона не повторювалася на кожній перевірці: тривога про пристрій, закрита через
  ×, повертається наступного дня, якщо досі актуальна); крім них — час спроб автоматичного скасування (для межі 5 на
  годину), скільки предметів має ваш власний інвентар на сервері Steam для кожної гри (лише кількості, без предметів),
  коли перевірка ваших трейдів почалася для вашого акаунта, ключований хеш партнера трейду, який цей браузер саме
  надсилає (10 хвилин), ваші власні трейди, скасовані десь інде (як хеші, 40 хвилин), скасування, що ще в черзі, і яка
  вкладка веде перевірку. Слова відкритої тривоги безпеки (назва й місце пристрою, SteamID і нікнейм партнера, номери
  трейдів, яких вона стосується) зберігаються лише в цій тривозі, доки ви на неї не відповісте чи не закриєте її, не довше
  24 годин; тривога про самозванця в чаті так само зберігає своїми словами два порівняні нікнейми й SteamID співрозмовника.
  Якщо вкладку «Трейд-офери» вимкнено, захист тримає фонове стеження за трейдами для своєї перевірки трейдів, з його
  звичними записами: SteamID вашого акаунта з лічильниками трейдів і номери прочитаних ним прийнятих надісланих трейдів.
  Список друзів вебчату та його відкриті особисті чати (імена, імена, які ви дали друзям, аватари; групові чати —
  ніколи) читаються на вашому комп’ютері, поки відкрита сторінка чату, і не зберігаються — крім слів відкритої тривоги
  (вище). Ваші сторінки вхідних і
  надісланих трейдів, прочитані для перевірки прихованих надісланих трейдів (з 1.12.1) і перевірки предметів трейду (з
  1.12.2: предмети кожного трейду), порівнюються з тим, що показує сторінка, у пам’яті й не зберігаються (їхні трейди,
  партнери, предмети та ігри предметів не зберігаються; лише тривога, яку здіймає одна з перевірок, зберігає своїми
  словами номери трейдів, яких вона стосується, — щонайбільше 10 — і, для прихованого трейду, надісланого не з цього
  браузера, SteamID і нікнейм його партнера, доки ви на неї не відповісте чи не закриєте її, не довше 24 годин). Нічого
  з цього нікуди не надсилається;
- (з 1.12.1) вартість ваших власних інвентарів біля балансу гаманця, для кожного акаунта (щонайбільше трьох): джерело
  цін, підсумки, кількості предметів і час — ніколи предмет, назва чи список, під SteamID акаунта;
- ваша відповідь на повідомлення про дані й ваше прийняття Ліцензійної угоди: лише її версія, час і ваш вибір щодо
  автоматизації (автоприйняття, автоскасування), без даних акаунта.

Кілька функцій сторінок також тримають невеликі значення у власному сховищі сайту Steam у вашому браузері
(`localStorage` та IndexedDB сайтів steamcommunity.com чи store.steampowered.com, як-от кеш цін ринку для
інструментів продажу та списки цін увімкнених вами джерел цін: назви предметів із цінами й кількостями, нічого про
вас; з 1.12.1, поки ввімкнено розмиття для стрімів, — котре з трьох увімкнено: гаманець, імена, аватари, щоб воно
діяло з першого кадру сторінки), як це роблять і самі сторінки Steam.

### 3. Ваша сесія Steam і токени
Коли ви користуєтеся сторінками Steam, код розширення на сторінці використовує ідентифікатор сесії та вебтокен,
які тримає сама відкрита сторінка Steam, і токени посилань для обміну. Вони використовуються **лише** в запитах до
Steam (`steamcommunity.com`, `store.steampowered.com`, `checkout.steampowered.com`, `api.steampowered.com`) — так
само, як їх використала б сторінка Steam. Ідентифікатор сесії й вебтокен розширення ніколи не зберігає й не передає
своїй фоновій частині. Токени посилань зберігаються лише всередині посилань, які ви зберегли (розділ 2). Жоден з них
нікуди більше не надсилається: фонова частина розширення відхиляє будь-який запит до не-Steam-сайту, схожий на
такий, що його містить.

### 4. Запити до Steam
Інструменти читають відкриті вами сторінки Steam і просять у Steam більше того самого (історію, описи предметів,
ціни, стан пропозицій) з вашою сесією Steam, як це зробила б сторінка. Інструменти наборів карток читають у Steam
подробиці ваших власних значків (набори карток, ваші рівні й XP), а сторінки значків публічного профілю — лише коли ви
просите рівні цього профілю. Крафт значків із наборів карток — це зміна у вашому акаунті: він надсилається до Steam
(по одному крафту) лише після того, як ви побачили план — ігри, набори й XP — і підтвердили його; його можна зупинити
будь-коли. Інші зміни у вашому акаунті надсилаються до Steam лише тоді, коли ви самі їх запускаєте: прийняття
вибраних вами пропозицій, виставлення предметів на продаж на торговельному майданчику (після перегляду цін або — коли
ви після попередження вибираєте «Продавати, щойно прочитано ціну» — кожен предмет, щойно прочитано його ціну) чи
зняття лотів, перетворення предметів на самоцвіти й відкриття наборів карток. Перший виняток — автоприйняття
(типово вимкнене): після вашої окремої згоди (власний прапорець
«Дозволити автоматичне прийняття вхідних подарункових трейдів», вимкнений, доки ви його не позначите) і коли ви його
ввімкнете, воно саме приймає вхідні пропозиції, в яких ви нічого не
віддаєте. Другий виняток — автоскасування Захисту від фішингу та скаму (з 1.12.0, типово «Вимкнено»): воно потребує
тієї самої згоди на автоматизацію (без неї налаштування читається як «Вимкнено»), і коли ви виберете «Лише за ознаками
фішингу» чи «Усі, надіслані не з цього браузера», воно саме скасовує трейди, надіслані з вашого акаунта не з цього
браузера, — один запит до Steam на трейд, не більше 5 спроб на годину (невдала спроба теж рахується); трейд,
надісланий з цього браузера, ніколи не скасовується, як і (з 1.12.1) трейд, що вже на утриманні або під захистом
трейду Steam (усе, що ви в ньому віддаєте, — предмети Counter-Strike 2), поки ввімкнено «Не скасовувати автоматично
трейди, що вже на утриманні (escrow) або під захистом трейду (trade protection)» (типово ввімкнено). Перевірки захисту лише читають із вашою сесією Steam: список
авторизованих пристроїв вашого акаунта (`api.steampowered.com` з вебтокеном сторінки, типово кожні 20 хвилин, з однієї
вкладки) і кожен третій раз сторінку Security & Devices (`store.steampowered.com/account/authorizeddevices`) для
рядків e-mail, телефону й Steam Guard (читається з відкритої вкладки `store.steampowered.com`; поки такої немає, ці
рядки чекають); ваші надіслані трейди — власними запитами фонового стеження за трейдами (його лічильники; його список
надісланих — коли ці лічильники змінюються, і не частіше ніж раз на 5 хвилин, поки якийсь ваш надісланий трейд чекає;
якщо вкладку «Трейд-офери» або її сповіщення про прийняті трейди вимкнено, ці читання списку робляться для цієї
перевірки; для тривоги про такий трейд — одне читання публічного профілю Steam його партнера, а за ознаки фішингу — і
партнера скасованого трейду, щоб тривога показала нікнейм); ваш власний інвентар із сервера Steam, щоб порівняти з
тим, що показує сторінка інвентаря, — коли ви відкриваєте свій інвентар (типово не частіше ніж раз на 6 годин;
приблизно один запит на гру й категорію предметів), а в проміжках лише його загальні кількості з однієї вкладки;
(з 1.12.1) вашу власну сторінку надісланих трейдів (`steamcommunity.com/…/tradeoffers/sent/`, адреса, яку ви відкрили),
коли ви її відкриваєте або вікно надісланого вами трейду, — не частіше ніж один запит на хвилину з однієї вкладки,
відповідь використовується 5 хвилин,
— лише щоб порівняти з тим, що показує сторінка (трейд, який щось у вашому браузері ховає); (з 1.12.2) вашу власну
сторінку вхідних трейдів (`steamcommunity.com/…/tradeoffers/`) так само, коли ви відкриваєте її або вікно одного з
ваших трейдів, і один раз для подарунка, що чекає на автоприйняття (не частіше ніж один запит на 10 секунд), — лише щоб
порівняти предмети, які показує кожен трейд, із власним записом Steam про нього (домальовані чи приховані предмети).
Друзі й діалоги вебчату читаються на самій сторінці чату, без запитів до серверів Steam — лише аватари схожих пар
завантажуються із серверів зображень Steam (avatars.fastly.steamstatic.com або власний хост аватарів сторінки чату), як їх завантажує й сама сторінка, без cookie й
реферера. Фонова частина звертається до публічного API
магазину Steam (`store.steampowered.com/api/appdetails`, `/api/packagedetails`) по ціни й зображення ігор і пакетів
без ваших cookie, а лише для перевірки інвентаря читає ваш власний інвентар (`steamcommunity.com/inventory/…`, нічого
іншого) з вашими cookie Steam, щоб жоден скрипт сторінки не бачив і не змінював відповіді: cookie додає сам браузер;
фонова частина їх не читає й не зберігає, не йде за переадресацією й не надсилає їх на жодну іншу адресу. Фонова
частина розширення так само читає й ваші сторінки надісланих (з 1.12.1) і вхідних (з 1.12.2) трейдів на
steamcommunity.com (лише ці дві адреси), тільки щоб порівняти їх з тим, що показує сторінка; нічого не зберігається.
(З 1.12.1) Вартість інвентаря біля балансу гаманця читає ваші власні інвентарі (TF2, CS2, Dota 2, Steam; Rust, якщо
ваше джерело цін його оцінює) зі Steam власними запитами сторінки, з однієї вкладки, по кліку на Σ або, коли вибрано
«Автоматично», сама кожні 30 хвилин, ніколи під час прийому чи надсилання трейду. Зображення предметів завантажуються
із серверів зображень Steam.

### 5. Додаткові сервіси
Три сайти репутації вмикаєте лише ви: на сторінці, що показується перед початком роботи Smart Trader (там їхній
прапорець вимкнений, доки ви його не позначите; браузер попросить дозволити сайти), або пізніше в параметрах розширення. Так само
й джерела цін (з 2026-10-09): marketdb.info, pricempire і публічні файли цін маркетплейсів (Market.CSGO та його сайти
TF2, Dota 2 і Rust, Waxpeer, LOOT.FARM, Lis-Skins) — кожне зі своїм прапорцем на тій сторінці (вимкненим, доки ви
його не позначите) або пізніше в параметрах; Smart Trader звертається до джерела, лише поки воно вибране джерелом цін
у налаштуваннях (до marketdb.info — також коли вибрано маркетплейс: його курси валют переводять ціни в доларах США, а
його списки цін оцінюють предмети, яких маркетплейс не оцінює, коли для «Предмети, яких маркетплейс не оцінює» вибрано
«marketdb.info після комісії Steam і комісії виведення»). marketdb.info — типове джерело цін Smart Trader (з 1.12.2): доки ви його не
ввімкнете, Smart Trader бере ціни з Ринку Steam.
Вони нічого не отримують про вас чи ваші предмети: лише гру, часове вікно чи маркетплейс цілого списку цін, а
pricempire — ще й ваш власний API-ключ. pricempire працює лише з вашим власним ключем вашого акаунта pricempire: ви
вводите його в налаштуваннях Smart Trader, він зберігається в сховищі розширення на цьому комп’ютері окремо від
налаштувань і надсилається лише до `api.pricempire.com` як заголовок `Authorization` його запитів, ніколи в адресі й
ніколи до іншого хоста (фонова частина розширення пересилає його лише туди й не зберігає копії); він ніколи не
показується на сторінці іншого сайту й не записується в діагностичний журнал. Сервер цін keys.land дозволений від початку (його хост встановлюється разом із розширенням),
і Smart Trader звертається до нього лише тоді, коли ці ціни увімкнені в налаштуваннях Smart Trader (KEYS.LAND →
«Використовувати ціни KEYS.LAND», з 1.12.2 увімкнено від початку; перемикач вкладки KEYS.LAND їх вимикає; з 1.12.4 —
єдиний перемикач цих цін із будь-яким джерелом цін, зокрема маркетплейсом), або — лише по показники обміну в Steam —
коли джерелом цін вибрано маркетплейс, а предмети, яких він не оцінює, оцінюються мінус автоматична комісія виведення,
або коли ціни Ринку Steam чи marketdb.info показуються як готівка («Готівка після комісії виведення», типово; завжди,
поки KEYS.LAND увімкнено); він нічого про вас не отримує. Вимкнути будь-який з них можна в параметрах будь-коли. Жоден з них не отримує від розширення cookie, крім SteamTrades: запит до SteamTrades несе ваші власні cookie
steamtrades.com, тож сайт відповідає так, як у вашій вкладці (це потрібно, щоб пройти його перевірку на ботів); це
відбувається лише коли SteamTrades увімкнено, лише в цьому одному запиті, а токени форм його сторінки вилучаються з
відповіді, перш ніж Smart Trader її читає. Кожен з них, як і
будь-який сайт, бачить вашу IP-адресу, назву й версію браузера (User-Agent) і час запиту.

| Сервіс | Що надсилається | Коли |
| --- | --- | --- |
| Сервер цін keys.land (хост, зазначений у дозволах розширення) | лише те, яка ціна потрібна: `GET …/kl/v1/market/series?item=key` (або `ticket`, `gems`) `&range=24h`; і показники обміну ключів, квитків і самоцвітів у Steam: `GET …/kl/v1/steam/convert` (без параметрів). Нічого про вас чи ваш обліковий запис. | коли показуються ціни ключів TF2, квитків чи самоцвітів (не частіше ніж раз на хвилину) — лише коли ціни KEYS.LAND увімкнені в налаштуваннях Smart Trader (з 1.12.2 увімкнено від початку; перемикач вкладки KEYS.LAND їх вимикає; з будь-яким джерелом цін, зокрема маркетплейсом); показники обміну — лише коли джерелом цін вибрано маркетплейс, а предмети, яких він не оцінює, оцінюються мінус автоматична комісія виведення, або коли ціни Ринку Steam чи marketdb.info показуються як готівка (типово; завжди, поки KEYS.LAND увімкнено) (не частіше ніж раз на кілька хвилин); сам сервер дозволений від початку, у параметрах його можна вимкнути |
| backpack.tf (`backpack.tf`) | публічний SteamID64 профілю чи партнера з обміну, якого ви переглядаєте: `GET https://backpack.tf/api/IGetUsers/v3?steamid=<SteamID64>` | коли ви відкриваєте профіль, пропозицію обміну чи історію обмінів |
| SteamTrades (`www.steamtrades.com`) | той самий SteamID64: `GET https://www.steamtrades.com/user/<SteamID64>`, з вашими власними cookie steamtrades.com (з 2026-10-07; потрібно, щоб пройти його перевірку на ботів) | так само |
| CSGO-Rep (`api.csgo-rep.com`) | той самий SteamID64: `POST https://api.csgo-rep.com` з `{"id": <число>, "query": {"steam_id": "<SteamID64>"}}`; час від часу `GET https://api.csgo-rep.com/config` (нічого про вас) | так само |
| marketdb.info (`marketdb.info`) | лише ідентифікатор гри й часове вікно цілого списку цін: `GET https://marketdb.info/api/v1/prices?game=<ідентифікатор гри>&hours=<24, 168 або 720>`; раз на день курси валют: `GET https://marketdb.info/api/v1/exchange-rates`. Нічого про вас чи ваші предмети, ніколи назви предмета. | коли показуються ціни гри, а збережений список старший за кілька годин — лише коли сервіс увімкнено і джерелом цін вибрано marketdb.info або маркетплейс (його курси валют, а його списки цін — коли «marketdb.info після комісії Steam і комісії виведення» оцінює предмети, яких маркетплейс не оцінює) |
| pricempire (`api.pricempire.com`) | ідентифікатор гри, маркетплейс і ваш власний API-ключ: `GET https://api.pricempire.com/v4/trader/items/prices?app_id=<ідентифікатор гри>&sources=<маркетплейс>&currency=USD` (з підпискою `/v4/paid/…`) із заголовком `Authorization: Bearer <ваш ключ>`; час від часу `GET https://api.pricempire.com/v4/free/status` (або `/limits`, `/currencies`) з тим самим заголовком. Більше нічого про вас чи ваші предмети. | коли показуються ціни CS2, а збережений список старший за час оновлення — лише коли pricempire вибрано джерелом цін і сервіс увімкнено |
| файли цін маркетплейсів (`market.csgo.com`, `tf2.tm`, `market.dota2.net`, `rust.tm`, `api.waxpeer.com`, `loot.farm`, `lis-skins.com`) | лише запит публічного файлу цін гри, наприклад `GET https://market.csgo.com/api/v2/prices/USD.json`, `GET https://api.waxpeer.com/v1/prices?game=csgo&minified=1`, `GET https://loot.farm/fullprice.json`, `GET https://lis-skins.com/market_export_json/csgo.json`. Нічого про вас чи ваші предмети, без ключа. | коли показуються ціни гри, а збережений список старший за дві години — лише з маркетплейсу, вибраного джерелом цін, і лише коли сервіс увімкнено |

Результати зберігаються на вашому комп’ютері кілька годин (розділ 2); списки джерел цін — лише як назви предметів із
цінами й кількостями. Сервер цін keys.land тримає автор Smart Trader;
він лише пересилає публічні дані про ціни з KEYS.LAND — незалежного сервісу, дані якого використовуються з дозволу його
власника. Сам сервер недовго зберігає лише звичайні журнали (запитану адресу й час) і нічого про ваш акаунт. backpack.tf,
SteamTrades, CSGO-Rep, marketdb.info, pricempire і маркетплейси застосовують власні умови й політики конфіденційності,
опубліковані на їхніх сайтах.

Коли ви вмикаєте backpack.tf, розширення також додає свої інструменти на відкриті вами сторінки backpack.tf (ціни
лотів у посиланнях на обмін, вартість рюкзака); доти воно там зовсім не працює. На цих сторінках сторінці передаються
лише ваші налаштування, стан підказок і значення самих інструментів backpack.tf; ваші збережені посилання для обміну,
партнери, записи пропозицій, результати перевірки репутації, історія покупок і діагностичний журнал — ні.

Картинки Unusual-ефектів (налаштування Smart Trader → Предмети й інвентар, типово вимкнено): коли ви їх вмикаєте,
браузер вантажить ці картинки з itempedia.tf (`https://itempedia.tf/assets/particles/<номер ефекту>_94x94.png`). Як і
будь-який сервер зображень, він бачить вашу IP-адресу, браузер і час; нічого іншого не надсилається.

3D-перегляд предметів CS2 (налаштування Smart Trader → Предмети й інвентар, типово ввімкнено): нічого не надсилається,
доки ви не натиснете «3D». Ваш клік відкриває нову вкладку вибраного вами переглядача (типово skinflow.gg;
csmarketcap.com чи swap.gg — з меню ▾), в адресі якої лише посилання огляду предмета — те саме, що Steam показує за «Inspect
in Game…». Першого разу Smart Trader спершу питає (це питання можна вимкнути). З 2026 року це посилання кодує сам
предмет: тип, фарбу, сід патерну, знос (флоат), наліпки й брелоки з їхнім розташуванням і зносом, лічильник StatTrak™,
текст іменного ярлика та ідентифікатор предмета, і в ньому може бути номер акаунта власника; старіше
посилання натомість містить SteamID64 власника (або ідентифікатор лота на ринку), ідентифікатор предмета й контрольне
число. Жодних cookie, сесії Steam, токена чи трейд-посилання з ним не йде; вкладка відкривається без реферера.
Переглядач бачить вашу IP-адресу, браузер і час і може передати посилання своїм власним сервісам (наприклад, своєму
3D-рендереру); діють його власні умови й політика конфіденційності. Панель
«Подробиці» розшифровує посилання на вашому комп’ютері й нічого не надсилає.

Посилання на інші сайти (наприклад, SteamDB, backpack.tf, SteamTrades, Steam Card Exchange) — звичайні посилання:
ці сайти нічого не отримують, доки ви не відкриєте посилання.

### 6. Діагностичний журнал
Діагностичний журнал (`dev.log`) вимкнений, доки ви його не ввімкнете (налаштування Smart Trader на сторінці Steam →
Загальні → Діагностика). Поки він увімкнений, він зберігає на вашому комп’ютері лише потрібне, щоб знайти помилки й
повільні місця: час, кількості, повідомлення про помилки (очищені) і стан мережевих запитів, не довше 7 днів і не
більше 4 МБ. Файл, який ви завантажуєте, також називає ваш браузер і його версію, операційну систему, клас розміру
екрана й щільність пікселів, мову інтерфейсу й зсув часового поясу, розширення чи рушій скриптів, що виконує Smart Trader, і його версію,
версії Smart Trader на цьому встановленні й коли його встановлено вперше, ваші налаштування як є (текстові — лише за
ключем, ніколи значення), стан його підказок і випадковий код цього встановлення, який відрізняє його журнали від
журналів іншого. Він ніколи не записує профілі: жодних SteamID, імен, аватарів, посилань на профілі чи обмін, токенів,
ідентифікаторів сесії чи адрес сторінок; ідентифікатори пропозицій і обмінів — лише як односторонні хеші із сіллю.
Він залишає ваш комп’ютер, лише якщо ви самі завантажите його («Завантажити журнал») і надішлете файл; «Очистити
журнал» видаляє його.

### 7. Чого розширення не робить
- Жодної аналітики, стеження, реклами чи партнерських посилань.
- Жодного продажу, оренди чи передавання ваших даних будь-кому, зокрема рекламним платформам, брокерам даних і
  перепродавцям інформації; жодного використання для оцінки кредитоспроможності чи кредитування.
- Ніхто з людей не читає ваших даних: ми (розробники) їх ніколи не отримуємо.
- Жодного віддаленого коду: увесь код розширення в його пакеті; відповіді з інтернету використовуються лише як дані.
- Усі запити йдуть через HTTPS.

**Limited Use.** Використання даних користувачів у Smart Trader відповідає політиці Chrome Web Store щодо даних
користувачів (Chrome Web Store User Data Policy), зокрема вимогам Limited Use.

### 8. Зберігання й видалення даних
Дані лишаються на вашому комп’ютері, доки ви їх не видалите. У параметрах розширення є «Видалити всі дані Smart
Trader» — це видаляє все з розділу 2, що лежить у сховищі розширення (крім вашої відповіді на повідомлення про
дані й вашого прийняття Ліцензійної угоди), і повертає браузеру доступ додаткових сервісів до їхніх сайтів. Видалення розширення теж видаляє його
сховище. Значення у власному сховищі сайту Steam (розділ 2) лишаються, доки ви не очистите дані цього сайту в
браузері. Кеші застарівають і скорочуються самі.

### 9. Зміни
Коли змінюється те, що розширення робить з даними, ця політика оновлюється, дата вгорі змінюється, а розширення
знову показує повідомлення про дані й чекає вашої згоди, перш ніж щось робити.

Зміни: 2026-10-07 — запит до SteamTrades несе ваші власні cookie steamtrades.com (розділ 5), лише коли SteamTrades
увімкнено. 2026-10-09 — додаткові джерела цін marketdb.info, pricempire (з вашим власним API-ключем) і публічні файли
цін маркетплейсів (розділи 2 і 5), кожне вимкнене, доки ви його не ввімкнете; сервер keys.land також дає показники
обміну в Steam. 2026-10-09 (1.12.0) — Захист від фішингу та скаму (розділи 2 і 4): список авторизованих пристроїв і
рядки e-mail, телефону й Steam Guard читаються зі Steam і зберігаються лише як односторонні хеші, ваш власний інвентар
читається з сервера Steam для перевірки на підміну (фоновою частиною, з вашими cookie Steam), друзі й особисті чати вебчату читаються на вашому комп’ютері, а
також додаткове автоскасування трейдів, надісланих не з цього браузера (типово вимкнене; потребує згоди на
автоматизацію). 2026-10-10 (1.12.1) — перевірка прихованих надісланих трейдів (розділи 2 і 4): ваша власна сторінка
надісланих трейдів, яку фонова частина читає з вашими cookie Steam лише щоб порівняти з тим, що показує сторінка,
нічого не зберігається (ті самі дані, які вже читає стеження за трейдами, тож нового повідомлення немає);
автоскасування ніколи не скасовує трейд, що вже на утриманні або під захистом трейду Steam (усе віддане в ньому —
предмети Counter-Strike 2), поки ввімкнено нове налаштування безпеки (типово ввімкнене); тривога про приховані трейди
зберігає своїми словами їхні номери (розділ 2); вартість інвентаря біля балансу гаманця зберігається лише як
підсумки (розділи 2 і 4); поки ввімкнено розмиття для стрімів — котрий з трьох його перемикачів увімкнено, у власному
сховищі сайту Steam (розділ 2). 2026-10-10 (1.12.2) — перевірка предметів трейду (розділи 2 і 4): також ваша власна
сторінка вхідних трейдів, яку фонова частина читає з вашими cookie Steam лише щоб порівняти предмети, які показує кожен
трейд, із власним записом Steam про нього, з цього не зберігається нічого, крім номерів трейдів у тривозі (розділ 2)
(ті самі дані, які вже читають стеження за трейдами й автоприйняття); ціни KEYS.LAND увімкнені від початку, а
marketdb.info — типове джерело цін Smart Trader (розділ 5): це оновлення один раз вмикає KEYS.LAND для кожного
встановлення (перемикач вкладки KEYS.LAND вимикає його знову), типово показує ціни Ринку Steam і marketdb.info як готівку
(показники обміну в Steam із сервера keys.land — той самий запит, що й раніше, тепер і для цього) і робить marketdb.info
типовим джерелом (до нього й далі звертаються лише після того, як ви ввімкнете його тут; доти ціни беруться з Ринку
Steam); 3D-перегляд предметів CS2 (розділ 5): переглядач відкривається в новій вкладці лише за вашим кліком, з
посиланням огляду предмета в адресі; до цього кліку нічого не надсилається. Оскільки KEYS.LAND і готівковий вигляд
вмикаються й для наявних встановлень, розширення знову показує повідомлення про дані (його версія 10). Ця версія
політики також називає те, чого попередні не називали: у розділі 2 — ваш власний нікнейм, предмети надісланих вами
трейдів, нікнейми й аватари збережених посилань для обміну, нікнейм партнера в записах прийнятих трейдів, робочі записи
перевірки чужих трейдів, слова тривоги про самозванця в чаті та вартість інвентаря, збережену під SteamID вашого
акаунта; у розділі 4 — одне читання публічного профілю партнера для нікнейму в тривозі та аватари схожих пар у чаті; у
розділі 6 — усе, що містить файл діагностичного журналу. 2026-10-10 (1.12.4) — провайдери цін працюють за однією
таблицею (розділ 5): «Використовувати ціни KEYS.LAND» — єдиний перемикач цих цін із будь-яким джерелом цін («Ключі,
білети й геми — за готівковою ціною KEYS.LAND» маркетплейсів тепер — цей перемикач), а ціни Ринку Steam чи marketdb.info
можна показувати як ціну ринку, як готівку чи як баланс Steam, який буде отримано; показники обміну із сервера keys.land
запитуються щоразу, коли вони показуються як готівка, з увімкненим чи вимкненим KEYS.LAND — той самий анонімний запит,
що й раніше, ніколи для ціни ринку чи балансу Steam.

### 10. Контакт
ggggggdev@gmail.com

Smart Trader — незалежний проєкт. Він не пов’язаний з Valve Corporation, не схвалений і не спонсорований нею. Steam і
логотип Steam — товарні знаки та/або зареєстровані товарні знаки Valve Corporation у США та/або інших країнах.

---

## Русский

**Действует с:** 2026-10-10 · **Контакт:** ggggggdev@gmail.com

Smart Trader добавляет инструменты для обмена на страницы Steam: сводки предложений обмена и цены предметов, более
быстрое принятие выбранных вами предложений, помощники для инвентаря и торговой площадки, итоги истории обменов,
проверку репутации партнёров, предупреждения о фишинге и скаме и уведомления на рабочем столе. Эта политика
описывает все данные, с которыми работает расширение, куда они уходят и как их удалить. Она соответствует коду
расширения; если код начнёт иначе обращаться с данными, изменятся и эта политика, и уведомление в расширении, а
расширение снова попросит вашего согласия, прежде чем что-либо делать.

### 1. Ничего не происходит без вашего согласия
После установки расширение показывает уведомление о данных. Пока вы не нажмёте «Согласен», оно ничего не делает на
страницах Steam: не читает данные страниц, ничего не сохраняет и не делает запросов.

### 2. Данные на вашем компьютере
Хранятся в хранилище расширения вашего браузера (`chrome.storage.local`) на этом компьютере и никому не отправляются,
в том числе нам:
- ваши настройки Smart Trader и состояние его панелей и туров;
- метки предметов и заметки, которые инструменты ведут о предметах;
- сохранённые вами ссылки для обмена (они содержат токен ссылки партнёра, а после прочтения — никнейм партнёра и адрес
  его аватара) и ваша собственная ссылка (с вашим никнеймом и адресом аватара);
- итоги и кеши с открытых вами страниц: итоги истории обменов и инвентаря, описания предметов, цены торговой
  площадки, результаты проверки репутации, списки друзей, записи принятых вами предложений (с никнеймом партнёра),
  история корзины магазина;
- ваш собственный никнейм для каждого аккаунта (сутки), чтобы уведомление на рабочем столе могло быть подписано им;
  предметы трейдов, отправленных из этого браузера (названия и изображения; 60 трейдов на аккаунт, 5 аккаунтов, не
  дольше 15 дней), чтобы уведомление о принятии такого трейда могло их назвать;
- ваши лоты, которые ещё ждут вашего подтверждения (в мобильном приложении Steam или по почте), чтобы инструменты
  продажи никогда не выставляли эти предметы снова; каждый хранится не дольше недели;
- то, что инструменты наборов карточек читают из ваших собственных значков Steam: размеры и списки карточек наборов,
  ваши уровни значков и сколько копий каждой карточки у вас есть (хранятся с односторонним хешем вашего аккаунта, так
  что другой аккаунт, входящий в этом браузере, их не видит), а также уровень и XP вашего аккаунта; уровни значков
  чужого профиля держатся только пока открыта его страница и не сохраняются;
- ваш выбор в параметрах расширения (дополнительные сервисы, звук);
- ваш API-ключ pricempire, если вы введёте его в настройках Smart Trader: хранится отдельно от настроек,
  отправляется только в pricempire (раздел 5) и никогда не показывается на странице другого сайта;
- (с 1.12.0) то, что нужно Защите от фишинга и скама (отдельная вкладка в настройках Smart Trader, по умолчанию
  включена), чтобы заметить изменение, — только как односторонние ключевые хеши (отпечатки, сделанные на этом
  компьютере со случайным ключом этой установки; самих данных из них не прочитать): сессии и устройства из списка
  авторизованных устройств вашего аккаунта и строки e-mail, телефона и Steam Guard вашего аккаунта; трейды,
  отправленные из этого браузера (не дольше 15 дней); трейды, которые вы отменяете на страницах трейдов Steam (не
  дольше 15 дней, чтобы собственная отмена никогда не принималась за признак фишинга); сессии, трейды и собеседники, которых вы отметили «Да, это я»
  или «Это другой человек»; сессии и трейды, о которых уже была тревога (чтобы она не повторялась на каждой проверке:
  тревога об устройстве, закрытая через ×, возвращается на следующий день, если всё ещё актуальна); кроме них — время
  попыток автоматической отмены (для предела 5 в час), сколько предметов в вашем собственном инвентаре на сервере Steam
  для каждой игры (только количества, без предметов), когда проверка ваших трейдов началась для вашего аккаунта,
  ключевой хеш партнёра трейда, который этот браузер сейчас отправляет (10 минут), ваши собственные трейды, отменённые
  где-то ещё (как хеши, 40 минут), отмены, ещё стоящие в очереди, и какая вкладка ведёт проверку. Слова открытой тревоги
  безопасности (название и место устройства, SteamID и никнейм партнёра, номера трейдов, которых она касается) хранятся только в
  этой тревоге, пока вы на неё не ответите или не закроете её, не дольше 24 часов; тревога о самозванце в чате так же
  хранит своими словами два сравнённых никнейма и SteamID собеседника. Если вкладка «Трейд-офферы» выключена, защита держит фоновое
  слежение за трейдами для своей проверки трейдов, с его обычными записями: SteamID вашего аккаунта со счётчиками
  трейдов и номера прочитанных им принятых отправленных трейдов. Список друзей веб-чата и его открытые личные чаты (имена, имена,
  которые вы дали друзьям, аватары; групповые чаты — никогда) читаются на вашем компьютере, пока открыта страница чата,
  и не сохраняются — кроме слов открытой тревоги (выше). Ваши страницы входящих и отправленных трейдов, прочитанные для проверки скрытых отправленных трейдов
  (с 1.12.1) и проверки предметов трейда (с 1.12.2: предметы каждого трейда), сравниваются с тем, что показывает
  страница, в памяти и не сохраняются (их трейды, партнёры, предметы и игры предметов не сохраняются; только тревога,
  которую поднимает одна из проверок, хранит своими словами номера трейдов, которых она касается, — не больше 10 — и,
  для скрытого трейда, отправленного не из этого браузера, SteamID и никнейм его партнёра, пока вы на неё не ответите
  или не закроете её, не дольше 24 часов). Ничего из этого никуда не отправляется;
- (с 1.12.1) стоимость ваших собственных инвентарей рядом с балансом кошелька, для каждого аккаунта (не больше трёх):
  источник цен, итоги, количества предметов и время — никогда предмет, название или список, под SteamID аккаунта;
- ваш ответ на уведомление о данных и ваше принятие Лицензионного соглашения: только его версия, время и ваш выбор
  насчёт автоматизации (автопринятия, автоотмены), без данных аккаунта.

Несколько функций страниц также хранят небольшие значения в собственном хранилище сайта Steam в вашем браузере
(`localStorage` и IndexedDB сайтов steamcommunity.com или store.steampowered.com, например кеш цен торговой
площадки для инструментов продажи и списки цен включённых вами источников цен: названия предметов с ценами и
количествами, ничего о вас; с 1.12.1, пока включено размытие для стримов, — какое из трёх включено: кошелёк, имена,
аватары, чтобы оно действовало с первого кадра страницы), как это делают и сами страницы Steam.

### 3. Ваша сессия Steam и токены
Когда вы пользуетесь страницами Steam, код расширения на странице использует идентификатор сессии и веб-токен,
которые держит сама открытая страница Steam, и токены ссылок для обмена. Они используются **только** в запросах к
Steam (`steamcommunity.com`, `store.steampowered.com`, `checkout.steampowered.com`, `api.steampowered.com`) — так же,
как их использовала бы страница Steam. Идентификатор сессии и веб-токен расширение никогда не сохраняет и не передаёт
своей фоновой части. Токены ссылок хранятся только внутри сохранённых вами ссылок (раздел 2). Ни один из них никуда
больше не отправляется: фоновая часть расширения отклоняет любой запрос к сайту не Steam, похожий на содержащий его.

### 4. Запросы к Steam
Инструменты читают открытые вами страницы Steam и запрашивают у Steam больше того же (историю, описания предметов,
цены, состояние предложений) с вашей сессией Steam, как это сделала бы страница. Инструменты наборов карточек читают у
Steam подробности ваших собственных значков (наборы карточек, ваши уровни и XP), а страницы значков публичного
профиля — только когда вы просите уровни этого профиля. Крафт значков из наборов карточек — это изменение в вашем
аккаунте: он отправляется в Steam (по одному крафту) только после того, как вы увидели план — игры, наборы и XP — и
подтвердили его; его можно остановить в любой момент. Остальные изменения в вашем аккаунте отправляются в Steam
только тогда, когда вы сами их запускаете: принятие выбранных вами предложений, выставление предметов на продажу на
торговой площадке (после просмотра цен или — когда вы после предупреждения выбираете «Продавать, как только прочитана
цена» — каждый предмет, как только прочитана его цена) или снятие лотов, превращение предметов в самоцветы и открытие
наборов карточек. Первое исключение — автопринятие (по умолчанию выключено): после вашего отдельного согласия (собственный
флажок «Разрешить автоматическое принятие входящих подарочных трейдов», выключен, пока вы его не отметите) и когда вы
его включите, оно само принимает входящие предложения, в которых вы ничего не отдаёте. Второе исключение — автоотмена
Защиты от фишинга и скама (с 1.12.0, по умолчанию «Выключено»): она требует того же согласия на автоматизацию (без
него настройка читается как «Выключено»), и когда вы выберете «Только по признакам фишинга» или «Все, отправленные не
из этого браузера», она сама отменяет трейды, отправленные с вашего аккаунта не из этого браузера, — один запрос к
Steam на трейд, не более 5 попыток в час (неудачная попытка тоже считается); трейд, отправленный из этого браузера,
никогда не отменяется, как и (с 1.12.1) трейд, уже находящийся на удержании или под защитой трейда Steam (всё, что вы в
нём отдаёте, — предметы Counter-Strike 2), пока включено «Не отменять автоматически трейды, уже находящиеся на
удержании (escrow) или под защитой трейда (trade protection)» (по умолчанию включено). Проверки защиты только читают с вашей сессией Steam: список авторизованных устройств вашего
аккаунта (`api.steampowered.com` с веб-токеном страницы, по умолчанию каждые 20 минут, из одной вкладки) и каждый
третий раз страницу Security & Devices (`store.steampowered.com/account/authorizeddevices`) для строк e-mail, телефона
и Steam Guard (читается из открытой вкладки `store.steampowered.com`; пока такой нет, эти строки ждут); ваши
отправленные трейды — собственными запросами фонового слежения за трейдами (его счётчики; его список отправленных —
когда эти счётчики меняются, и не чаще раза в 5 минут, пока какой-то ваш отправленный трейд ждёт; если вкладка
«Трейд-офферы» или её уведомление о принятых трейдах выключены, эти чтения списка делаются для этой проверки; для
тревоги о таком трейде — одно чтение публичного профиля Steam его партнёра, а по признаку фишинга — и партнёра
отменённого трейда, чтобы тревога показала никнейм); ваш собственный инвентарь с сервера Steam, чтобы сравнить с тем,
что показывает страница инвентаря, — когда вы открываете свой инвентарь (по умолчанию не чаще раза в 6 часов; примерно
один запрос на игру и категорию предметов), а в промежутках только его общие количества из одной вкладки; (с 1.12.1)
вашу собственную страницу отправленных трейдов (`steamcommunity.com/…/tradeoffers/sent/`, адрес, который вы открыли), когда
вы её открываете или окно отправленного вами трейда, — не чаще одного запроса в минуту из одной вкладки, ответ
используется 5 минут, — только чтобы
сравнить с тем, что показывает страница (трейд, который что-то в вашем браузере скрывает); (с 1.12.2) вашу
собственную страницу входящих трейдов (`steamcommunity.com/…/tradeoffers/`) так же, когда вы открываете её или окно
одного из ваших трейдов, и один раз для подарка, ожидающего автопринятия (не чаще одного запроса в 10 секунд), — только
чтобы сравнить предметы, которые показывает каждый трейд, с собственной записью Steam о нём (дорисованные или скрытые
предметы). Друзья и диалоги веб-чата читаются на самой странице чата, без запросов к серверам Steam — только аватары
похожих пар загружаются с серверов изображений Steam (avatars.fastly.steamstatic.com или собственный хост аватаров страницы чата), как их загружает и сама страница, без
cookie и реферера. Фоновая часть обращается к публичному API магазина
Steam (`store.steampowered.com/api/appdetails`, `/api/packagedetails`) за ценами и изображениями игр и пакетов без
ваших cookie, а только для проверки инвентаря читает ваш собственный инвентарь (`steamcommunity.com/inventory/…`,
ничего другого) с вашими cookie Steam, чтобы ни один скрипт страницы не видел и не менял ответа: cookie добавляет сам
браузер; фоновая часть их не читает и не хранит, не следует переадресации и не отправляет их ни на какой другой адрес.
Фоновая часть расширения так же читает и ваши страницы отправленных (с 1.12.1) и входящих (с 1.12.2) трейдов на
steamcommunity.com (только эти два адреса), только чтобы сравнить их с тем, что показывает страница; ничего не
сохраняется. (С 1.12.1) Стоимость инвентаря рядом с балансом кошелька читает ваши собственные инвентари (TF2, CS2,
Dota 2, Steam; Rust, если ваш источник цен его оценивает) из Steam собственными запросами страницы, из одной вкладки,
по клику на Σ или, когда выбрано «Автоматически», сама каждые 30 минут, никогда во время приёма или отправки трейда.
Изображения предметов загружаются с серверов изображений Steam.

### 5. Дополнительные сервисы
Три сайта репутации включаете только вы: на странице, показанной перед началом работы Smart Trader (там их флажок
выключен, пока вы его не отметите; браузер попросит разрешить сайты), или позже в параметрах расширения. Так же и
источники цен (с 2026-10-09): marketdb.info, pricempire и публичные файлы цен маркетплейсов (Market.CSGO и его сайты
TF2, Dota 2 и Rust, Waxpeer, LOOT.FARM, Lis-Skins) — каждый со своим флажком на той странице (выключенным, пока вы
его не отметите) или позже в параметрах; Smart Trader обращается к источнику, только пока он выбран источником цен в
настройках (к marketdb.info — также когда выбран маркетплейс: его курсы валют переводят цены в долларах США, а его
списки цен оценивают предметы, которые маркетплейс не оценивает, когда для «Предметы, которые маркетплейс не оценивает»
выбрано «marketdb.info после комиссии Steam и комиссии вывода»). marketdb.info — источник цен Smart Trader по умолчанию (с 1.12.2): пока
вы его не включите, Smart Trader берёт цены с Рынка Steam. Они
ничего не получают о вас или ваших предметах: только игру, временное окно или маркетплейс целого списка цен, а
pricempire — ещё и ваш собственный API-ключ. pricempire работает только с вашим собственным ключом вашего аккаунта
pricempire: вы вводите его в настройках Smart Trader, он хранится в хранилище расширения на этом компьютере отдельно от
настроек и отправляется только на `api.pricempire.com` как заголовок `Authorization` его запросов, никогда в адресе и
никогда на другой хост (фоновая часть расширения пересылает его только туда и не хранит копии); он никогда не
показывается на странице другого сайта и не записывается в диагностический журнал. Сервер цен keys.land разрешён с самого начала (его хост устанавливается вместе с
расширением), и Smart Trader обращается к нему только тогда, когда эти цены включены в настройках Smart Trader
(KEYS.LAND → «Использовать цены KEYS.LAND», с 1.12.2 включено с самого начала; переключатель вкладки KEYS.LAND их
выключает; с 1.12.4 — единственный переключатель этих цен с любым источником цен, в том числе маркетплейсом), или —
только за показателями обмена в Steam — когда источником цен выбран маркетплейс, а предметы, которые он не оценивает,
оцениваются минус автоматическая комиссия вывода, или когда цены Рынка Steam или marketdb.info показываются как наличные
(«Наличные после комиссии вывода», по умолчанию; всегда, пока KEYS.LAND включён); он ничего о вас не получает. Выключить любой из них можно в параметрах в любой момент. Ни один из них не получает от расширения cookie, кроме SteamTrades: запрос к SteamTrades несёт ваши собственные
cookie steamtrades.com, поэтому сайт отвечает так же, как в вашей вкладке (это нужно, чтобы пройти его проверку на
ботов); это происходит только когда SteamTrades включён, только в этом одном запросе, а токены форм его страницы
удаляются из ответа, прежде чем Smart Trader его читает. Каждый из
них, как и любой сайт, видит ваш IP-адрес, название и версию браузера (User-Agent) и время запроса.

| Сервис | Что отправляется | Когда |
| --- | --- | --- |
| Сервер цен keys.land (хост, указанный в разрешениях расширения) | только то, какая цена нужна: `GET …/kl/v1/market/series?item=key` (или `ticket`, `gems`) `&range=24h`; и показатели обмена ключей, билетов и самоцветов в Steam: `GET …/kl/v1/steam/convert` (без параметров). Ничего о вас или вашей учётной записи. | когда показываются цены ключей TF2, билетов или самоцветов (не чаще раза в минуту) — только когда цены KEYS.LAND включены в настройках Smart Trader (с 1.12.2 включено с самого начала; переключатель вкладки KEYS.LAND их выключает; с любым источником цен, в том числе маркетплейсом); показатели обмена — только когда источником цен выбран маркетплейс, а предметы, которые он не оценивает, оцениваются минус автоматическая комиссия вывода, или когда цены Рынка Steam или marketdb.info показываются как наличные (по умолчанию; всегда, пока KEYS.LAND включён) (не чаще раза в несколько минут); сам сервер разрешён с самого начала, в параметрах его можно выключить |
| backpack.tf (`backpack.tf`) | публичный SteamID64 профиля или партнёра по обмену, которого вы просматриваете: `GET https://backpack.tf/api/IGetUsers/v3?steamid=<SteamID64>` | когда вы открываете профиль, предложение обмена или историю обменов |
| SteamTrades (`www.steamtrades.com`) | тот же SteamID64: `GET https://www.steamtrades.com/user/<SteamID64>`, с вашими собственными cookie steamtrades.com (с 2026-10-07; нужно, чтобы пройти его проверку на ботов) | так же |
| CSGO-Rep (`api.csgo-rep.com`) | тот же SteamID64: `POST https://api.csgo-rep.com` с `{"id": <число>, "query": {"steam_id": "<SteamID64>"}}`; время от времени `GET https://api.csgo-rep.com/config` (ничего о вас) | так же |
| marketdb.info (`marketdb.info`) | только идентификатор игры и временное окно целого списка цен: `GET https://marketdb.info/api/v1/prices?game=<идентификатор игры>&hours=<24, 168 или 720>`; раз в день курсы валют: `GET https://marketdb.info/api/v1/exchange-rates`. Ничего о вас или ваших предметах, никогда названия предмета. | когда показываются цены игры, а сохранённый список старше нескольких часов — только когда сервис включён и источником цен выбран marketdb.info или маркетплейс (его курсы валют, а его списки цен — когда «marketdb.info после комиссии Steam и комиссии вывода» оценивает предметы, которые маркетплейс не оценивает) |
| pricempire (`api.pricempire.com`) | идентификатор игры, маркетплейс и ваш собственный API-ключ: `GET https://api.pricempire.com/v4/trader/items/prices?app_id=<идентификатор игры>&sources=<маркетплейс>&currency=USD` (с подпиской `/v4/paid/…`) с заголовком `Authorization: Bearer <ваш ключ>`; время от времени `GET https://api.pricempire.com/v4/free/status` (или `/limits`, `/currencies`) с тем же заголовком. Больше ничего о вас или ваших предметах. | когда показываются цены CS2, а сохранённый список старше времени обновления — только когда pricempire выбран источником цен и сервис включён |
| файлы цен маркетплейсов (`market.csgo.com`, `tf2.tm`, `market.dota2.net`, `rust.tm`, `api.waxpeer.com`, `loot.farm`, `lis-skins.com`) | только запрос публичного файла цен игры, например `GET https://market.csgo.com/api/v2/prices/USD.json`, `GET https://api.waxpeer.com/v1/prices?game=csgo&minified=1`, `GET https://loot.farm/fullprice.json`, `GET https://lis-skins.com/market_export_json/csgo.json`. Ничего о вас или ваших предметах, без ключа. | когда показываются цены игры, а сохранённый список старше двух часов — только с маркетплейса, выбранного источником цен, и только когда сервис включён |

Результаты хранятся на вашем компьютере несколько часов (раздел 2); списки источников цен — только как названия
предметов с ценами и количествами. Сервер цен keys.land держит автор Smart Trader;
он только пересылает публичные данные о ценах с KEYS.LAND — независимого сервиса, данные которого используются с
разрешения его владельца. Сам сервер недолго хранит только обычные журналы (запрошенный адрес и время) и ничего о вашем
аккаунте. backpack.tf, SteamTrades, CSGO-Rep, marketdb.info, pricempire и маркетплейсы применяют собственные условия
и политики конфиденциальности, опубликованные на их сайтах.

Когда вы включаете backpack.tf, расширение также добавляет свои инструменты на открытые вами страницы backpack.tf
(цены лотов в ссылках на обмен, стоимость рюкзака); до этого оно там вовсе не работает. На этих страницах странице
передаются только ваши настройки, состояние подсказок и значения самих инструментов backpack.tf; ваши сохранённые
ссылки для обмена, партнёры, записи предложений, результаты проверки репутации, история покупок и диагностический
журнал — нет.

Картинки Unusual-эффектов (настройки Smart Trader → Предметы и инвентарь, по умолчанию выключено): когда вы их
включаете, браузер загружает эти картинки с itempedia.tf (`https://itempedia.tf/assets/particles/<номер эффекта>_94x94.png`).
Как и любой сервер изображений, он видит ваш IP-адрес, браузер и время; ничего другого не отправляется.

3D-просмотр предметов CS2 (настройки Smart Trader → Предметы и инвентарь, по умолчанию включено): ничего не
отправляется, пока вы не нажмёте «3D». Ваш клик открывает новую вкладку выбранного вами просмотрщика (по умолчанию
skinflow.gg; csmarketcap.com или swap.gg — из меню ▾), в адресе которой только ссылка осмотра предмета — та же, что Steam
показывает за «Inspect in Game…». В первый раз Smart Trader сначала спрашивает (этот вопрос можно выключить). С 2026 года
эта ссылка кодирует сам предмет: тип, раскраску, сид паттерна, износ (флоат), наклейки и брелоки с их расположением и
износом, счётчик StatTrak™, текст именного ярлыка и идентификатор предмета, и в ней может быть номер аккаунта
владельца; более старая ссылка вместо этого содержит SteamID64 владельца (или идентификатор лота на рынке),
идентификатор предмета и контрольное число. Никаких cookie, сессии Steam, токена или трейд-ссылки с ней не уходит;
вкладка открывается без реферера. Просмотрщик видит ваш IP-адрес, браузер и время и может передать ссылку своим
собственным сервисам (например, своему 3D-рендереру); действуют его собственные условия и политика конфиденциальности. Панель «Подробности» расшифровывает ссылку на вашем компьютере и ничего не отправляет.

Ссылки на другие сайты (например, SteamDB, backpack.tf, SteamTrades, Steam Card Exchange) — обычные ссылки: эти
сайты ничего не получают, пока вы не откроете ссылку.

### 6. Диагностический журнал
Диагностический журнал (`dev.log`) выключен, пока вы его не включите (настройки Smart Trader на странице Steam → Общие
→ Диагностика). Пока он включён, он хранит на вашем компьютере только нужное, чтобы найти ошибки и медленные места:
время, количества, сообщения об ошибках (очищенные) и состояние сетевых запросов, не дольше 7 дней и не больше 4 МБ.
Файл, который вы скачиваете, также называет ваш браузер и его версию, операционную систему, класс размера экрана и плотность
пикселей, язык интерфейса и смещение часового пояса, расширение или движок скриптов, выполняющий Smart Trader, и его версию, версии
Smart Trader на этой установке и когда она была сделана впервые, ваши настройки как есть (текстовые — только по ключу,
никогда значение), состояние его подсказок и случайный код этой установки, отличающий его журналы от журналов другой.
Он никогда не записывает профили: никаких SteamID, имён, аватаров, ссылок на профили или обмен, токенов,
идентификаторов сессии или адресов страниц; идентификаторы предложений и обменов — только как односторонние хеши с
солью. Он покидает ваш компьютер, только если вы сами скачаете его («Скачать журнал») и отправите файл; «Очистить
журнал» удаляет его.

### 7. Чего расширение не делает
- Никакой аналитики, слежки, рекламы или партнёрских ссылок.
- Никакой продажи, аренды или передачи ваших данных кому-либо, в том числе рекламным платформам, брокерам данных и
  перепродавцам информации; никакого использования для оценки кредитоспособности или кредитования.
- Никто из людей не читает ваши данные: мы (разработчики) их никогда не получаем.
- Никакого удалённого кода: весь код расширения в его пакете; ответы из интернета используются только как данные.
- Все запросы идут через HTTPS.

**Limited Use.** Использование данных пользователей в Smart Trader соответствует политике Chrome Web Store в отношении
данных пользователей (Chrome Web Store User Data Policy), включая требования Limited Use.

### 8. Хранение и удаление данных
Данные остаются на вашем компьютере, пока вы их не удалите. В параметрах расширения есть «Удалить все данные Smart
Trader» — это удаляет всё из раздела 2, что лежит в хранилище расширения (кроме вашего ответа на уведомление о
данных и вашего принятия Лицензионного соглашения), и возвращает браузеру доступ дополнительных сервисов к их сайтам. Удаление расширения тоже удаляет его
хранилище. Значения в собственном хранилище сайта Steam (раздел 2) остаются, пока вы не очистите данные этого сайта в
браузере. Кеши устаревают и сокращаются сами.

### 9. Изменения
Когда меняется то, что расширение делает с данными, эта политика обновляется, дата вверху меняется, а расширение снова
показывает уведомление о данных и ждёт вашего согласия, прежде чем что-либо делать.

Изменения: 2026-10-07 — запрос к SteamTrades несёт ваши собственные cookie steamtrades.com (раздел 5), только когда
SteamTrades включён. 2026-10-09 — дополнительные источники цен marketdb.info, pricempire (с вашим собственным
API-ключом) и публичные файлы цен маркетплейсов (разделы 2 и 5), каждый выключен, пока вы его не включите; сервер
keys.land также даёт показатели обмена в Steam. 2026-10-09 (1.12.0) — Защита от фишинга и скама (разделы 2 и 4):
список авторизованных устройств и строки e-mail, телефона и Steam Guard читаются из Steam и хранятся только как
односторонние хеши, ваш собственный инвентарь читается с сервера Steam для проверки на подмену (фоновой частью, с вашими cookie Steam), друзья и личные чаты
веб-чата читаются на вашем компьютере, а также дополнительная автоотмена трейдов, отправленных не из этого браузера
(по умолчанию выключена; требует согласия на автоматизацию). 2026-10-10 (1.12.1) — проверка скрытых отправленных
трейдов (разделы 2 и 4): ваша собственная страница отправленных трейдов, которую фоновая часть читает с вашими cookie
Steam только чтобы сравнить с тем, что показывает страница, ничего не сохраняется (те же данные, которые уже читает
слежение за трейдами, поэтому нового уведомления нет); автоотмена никогда не отменяет трейд, уже находящийся на
удержании или под защитой трейда Steam (всё отданное в нём — предметы Counter-Strike 2), пока включена новая настройка
безопасности (по умолчанию включена); тревога о скрытых трейдах хранит своими словами их номера (раздел 2); стоимость
инвентаря рядом с балансом кошелька хранится только как итоги (разделы 2 и 4); пока включено размытие для стримов —
какой из трёх его переключателей включён, в собственном хранилище сайта Steam (раздел 2). 2026-10-10 (1.12.2) —
проверка предметов трейда (разделы 2 и 4): также ваша собственная страница входящих трейдов, которую фоновая часть
читает с вашими cookie Steam только чтобы сравнить предметы, которые показывает каждый трейд, с собственной записью Steam
о нём, из этого не сохраняется ничего, кроме номеров трейдов в тревоге (раздел 2) (те же данные, которые уже читают
слежение за трейдами и автопринятие); цены KEYS.LAND включены с самого начала, а marketdb.info — источник цен Smart
Trader по умолчанию (раздел 5): это обновление один раз включает KEYS.LAND для каждой установки (переключатель вкладки
KEYS.LAND выключает его снова), по умолчанию показывает цены Рынка Steam и marketdb.info как наличные (показатели обмена
в Steam с сервера keys.land — тот же запрос, что и раньше, теперь и для этого) и делает marketdb.info источником по
умолчанию (к нему по-прежнему обращаются только после того, как вы включите его здесь; до того цены берутся с Рынка
Steam); 3D-просмотр предметов CS2 (раздел 5): просмотрщик открывается в новой вкладке только по вашему клику, со
ссылкой осмотра предмета в адресе; до этого клика ничего не отправляется. Поскольку KEYS.LAND и наличный вид включаются
и для существующих установок, расширение снова показывает уведомление о данных (его версия 10). Эта версия политики
также называет то, чего прежние не называли: в разделе 2 — ваш собственный никнейм, предметы отправленных вами трейдов,
никнеймы и аватары сохранённых ссылок для обмена, никнейм партнёра в записях принятых трейдов, рабочие записи проверки
чужих трейдов, слова тревоги о самозванце в чате и стоимость инвентаря, сохранённую под SteamID вашего аккаунта; в
разделе 4 — одно чтение публичного профиля партнёра для никнейма в тревоге и аватары похожих пар в чате; в разделе 6 —
всё, что содержит файл диагностического журнала. 2026-10-10 (1.12.4) — источники цен работают по одной таблице (раздел
5): «Использовать цены KEYS.LAND» — единственный переключатель этих цен с любым источником цен («Ключи, билеты и гемы —
по наличной цене KEYS.LAND» маркетплейсов теперь — этот переключатель), а цены Рынка Steam или marketdb.info можно
показывать как цену рынка, как наличные или как баланс Steam, который будет получен; показатели обмена с сервера
keys.land запрашиваются всякий раз, когда они показываются как наличные, с включённым или выключенным KEYS.LAND — тот
же анонимный запрос, что и раньше, никогда для цены рынка или баланса Steam.

### 10. Контакт
ggggggdev@gmail.com

Smart Trader — независимый проект. Он не связан с Valve Corporation, не одобрен и не спонсируется ею. Steam и логотип
Steam — товарные знаки и/или зарегистрированные товарные знаки Valve Corporation в США и/или других странах.
