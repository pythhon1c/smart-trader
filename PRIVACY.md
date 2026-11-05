# Smart Trader – privacy policy

Effective since 2026-10-31, for the browser extension. The same text in three languages: [English](#english) · [Українська](#українська) · [Русский](#русский).

---

## English

**Effective date:** 2026-10-31 · **Contact:** ggggggdev@gmail.com

Smart Trader adds trading tools to Steam pages: trade offer summaries and item prices, faster accepting of the offers
you choose, inventory and Community Market helpers, trade history summaries, partner reputation checks, phishing and
scam warnings and desktop alerts. This policy describes every piece of data the extension handles, where it goes and
how to delete it. It matches the extension's code; if the code changes what it does with data, this policy and the
in-extension notice change with it, and the extension asks for your agreement again before doing anything.

### 1. Nothing happens before you agree
After installation the extension shows a data notice. Until you press "I agree", nothing runs on Steam pages and no
request is sent; only the installation's own service state is stored (which optional services are on, diagnostic
counters), with no personal data.

### 2. Data kept on your computer
Stored in your browser on this computer — in the extension's storage (`chrome.storage.local`) and, since 1.21.0, the
bigger caches in the Steam sites' own IndexedDB (see after this list) — never sent to us or anyone:
- your Smart Trader settings and the state of its panels and tours;
- item marks and the notes the tools keep about items;
- trade links you save (they contain the partner's trade link token and, once read, the partner's nickname and avatar
  address) and your own trade link (with your nickname and avatar address);
- summaries and caches built from pages you opened: trade and inventory history summaries, item descriptions,
  Community Market prices, partner reputation results, friends lists, records of offers you accepted (with the
  partner's nickname), the store cart history; the prices of keys, tickets and gems last read from the KEYS.LAND
  Telegram channel (six prices, the post's number and time, when the page was read and why the last read failed, if it
  did: a week at most);
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
- whether the tools on backpack.tf's pages may run: one yes / no that Smart Trader's code on Steam's pages copies
  from its settings ("backpack.tf pages" and the game switch "Team Fortress 2"), so that the extension's background
  part loads those tools on backpack.tf only while both are on;
- your pricempire API key, if you set one on the extension's options page (never on a website; since 1.21.9, before in
  Smart Trader's settings): kept in the extension's own storage apart from the settings (its own database, which no web
  page and no part of the extension running in a page can read), never handed to Steam's pages, sent only to pricempire
  (section 5) by the extension's background part;
- (since 1.18.0) your steamapis.com API key, if you set one on the extension's options page (never on a website): kept in the extension's own storage apart from the settings (its own database, which no web page and no part of the extension running in a page can read), never handed to Steam's pages, sent only to steamapis.com
  (section 5) by the extension's background part; and, on this browser only, how many requests went through it (this
  month, today) and their usual time;
- (since 1.12.0) what the Phishing and scam protection (its own tab in Smart Trader's settings; since 1.19.2 an
  experimental feature, off by default: nothing in this item is read or kept until you turn one of its checks on; since 1.22.0 each check is its own switch) needs to
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
  the offer watch off, the protection keeps the background offer watch running for its trade check, with that
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
- (since 1.21.23) Steam's own exchange rates of the currencies in use (your wallet's and the one chosen in "Show prices
  in"): each rate with the time it was read, the market id of the reference item it was read from and, after a failed
  read, its time and how many failed in a row — nothing about you; a rate is used for a week at most, "Clear price
  cache" (General → Tools) deletes them;
- (since 1.21.23) for the blinking button in Steam's header, per account under its SteamID: the ids of your sent trade
  offers that await your confirmation in the Steam Mobile app or by e-mail (100 at most, each 15 days at most) and the
  times of the offers sent from this browser in the last hour (20 at most); removed while that button's setting is off;
- (since 1.22.0) for the item counts in Steam's header, per account under its SteamID (three accounts at most): besides
  each inventory's count and when it was read, the trades on hold whose items those counts wait for (the offer's id,
  when Steam ends the hold and which of your inventories — game and context numbers — its items come into; 50 at most,
  each until a day after its hold ends) and the time of the newest trade seen on your own trade history or offers
  pages — counts, ids and times only, no item names;
- (since 1.22.0) Quick accept's pace: how many milliseconds per item Steam took in the clean accepts of 20 items or
  more in this browser (the last 10 per game and of all games), for its countdown and its longer waits while Steam is
  slow — numbers only, no offer and no account;
- (since 1.22.0) when the sales notifications of the Notifications tab are on ("Sales on the Steam Market", off unless
  you turn them on), one record for the browser's account, under its SteamID (a different account signed in starts it
  over, telling nothing of the one before): the newest sales of your own Steam Market listings this browser has seen and
  not told you of yet (the item's market name, what the buyer paid and what you received with Steam's id of their
  currency, the sale's time — for the newest 12; for older ones only their count and the totals per currency, with the
  oldest one's time), the time of the newest event of your market history (a listing created or cancelled, a purchase,
  a sale) with Steam's listing and purchase ids of that second's sales only (to count each sale once), and the times of
  the last read of your market history and of the last notification — for the one notification per period; nothing
  about the buyer; turning the notifications off leaves it as it is, "Delete all Smart Trader data" deletes it;
- (since 1.16.1) how many trades you had with each trade partner and the days of the first and last one, kept as
  one-way keyed hashes of the partner's SteamID with counts and days only (no names, no items), per account (five at
  most, 2,000 partners each), together with keyed hashes of the newest 4,000 trades (of the offer's id, or of the
  partner with the minute of the trade) and their days, to count each trade once, and how far the trade history was
  read, built from the trade history pages you open, the offers you accept and your sent offers the offer watch reads
  as accepted; the Phishing and scam protection shows "No trade since <date>" on an offer from a
  partner not in it. Nothing is sent anywhere; "Forget partner history" (Smart Trader's settings → Phishing and scam
  protection) deletes it;
- your answer to the data notice and your acceptance of the License Agreement: only its version, the time and your
  choice about automation (auto accept, auto-cancel), with no account data; (since 1.22.0) the extension's options page
  (Overview) shows them in a diagnostic line under the data notice with the state of the optional services and the
  extension's id, together with counts kept only in the browser's memory until it closes: how many times the notice
  was shown since the browser started and why, and how many reads of the extension's storage failed.

Since 1.21.0 the bigger of these records are not in the extension's storage but in the Steam sites' own IndexedDB in
your browser (a database named `ct-cache` of steamcommunity.com, and of store.steampowered.com when the store's pages
use these caches): the item descriptions (on a Steam page in a language other than English with the English ones of
section 4: at most 20,000 item classes there, 5,000 otherwise; an English one is asked again after 30 days), the
Community Market prices and the order books' prices, the card sets and badge levels, the items of the offers you sent,
the partner history, the Quick accept timing log (offer ids only as short codes), the item names the header's settings
suggest and (since 1.21.18) the Fear & Greed index's history of the order book of each item page you open (the time,
the numbers of listings and buy orders, the spread and the index: one row an hour for 7 days, one a day before them, 30
days and 500 items at most). None of it is sent anywhere. "Clear item info cache" (the descriptions, the card sets and
levels, the suggested names) and "Clear price cache" (the prices and the Fear & Greed history) in Smart Trader's
settings → General → Tools, and "Forget partner history", delete them; since 1.21.24 "Delete all Smart Trader data" on
the extension's options page deletes this database too, with Smart Trader's other databases on Steam's sites (section
8).

A few page features also keep small values in the Steam site's own storage in your browser (`localStorage` and
IndexedDB of steamcommunity.com or store.steampowered.com, for example the market price caches of the selling tools,
and the price lists of the price sources you turned on: item names with their prices and counts, nothing about you;
since 1.22.0 also one list of CS2 prices (the Steam Market and five marketplaces) that the keys.land relay hands over from cs2.sh, kept 15 minutes by default ("cs2.sh list: ask again after" in the CS2 tab), item names with prices and counts and nothing about you, deleted by "Clear" in Price providers; also the marketplace ids of CS2 items (Buff, Youpin, C5GAME) for the links in the item card, one file from the same relay kept 24 hours, nothing about you, deleted by the same "Clear";
since 1.12.1, while a blur for streams is on, which of the three is on — the wallet, names, avatars — so that it holds
from a page's first frame; since 1.22.0, which settings tabs' "Advanced settings" block you left open), as Steam's
pages do themselves. Since 1.21.24 "Delete all Smart Trader data" deletes these
IndexedDB databases as well (section 8); the few `localStorage` values stay until you clear that site's data in the
browser. Two settings also write one of Steam's own preference cookies, as Steam's own buttons do: "Load Steam's
classic market pages instead of its Market Beta" (Selling & market; on by default for new installations since 1.21.18)
writes `bMarketOptOut` on steamcommunity.com/market — the value of Steam's own "Exit Market Beta" button, so that Steam
serves its classic market pages where it still has them; turned off, the extension removes the one it wrote — and "Skip
the store's age check" (Steam store, on by default) writes `birthtime` on store.steampowered.com, a fixed date of birth
(1 January 1980) that answers the store's age check. Steam reads them with its pages; they hold nothing about you and go
nowhere else.

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
offer states) with your Steam session, as the page would. (Since 1.21.23) On a Steam page in a language other than English they also
ask Steam for the English description of a TF2 or CS2 item class whose lines they cannot read in that language (at
most 200 a page visit, in the background; kept with the item descriptions of section 2 and asked again after 30
days); this goes only to Steam. (Since 1.22.0) While the sales notifications of the Notifications tab are on, one tab
of the browser reads your own Steam Market history (`steamcommunity.com/market/myhistory/`) with your Steam session once
per the period you chose (15 minutes by default), for the newest sales of your own listings; nothing is sent to anyone.
The card set tools read your own badges' details from Steam
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
minutes while one of your sent offers is waiting — with the offer watch or its notification of accepted offers
off, these list reads are made for this check; for an alert about such an offer, one read of its partner's public
Steam profile — and, on a phishing sign, of the cancelled offer's partner — for the nickname the alert shows); your own
inventory from Steam's server, to compare with what the inventory page shows — when you open your
inventory (at most once every 6 hours by default; about one request per game and item category) and, in between, its
totals alone from one tab; (since 1.12.1) your own sent offers page (`steamcommunity.com/…/tradeoffers/sent/`, the address you have open),
when you open it or the window of an offer you sent — at most one request a minute from one tab, its answer used for 5
minutes —, only to compare it with
what the page shows (an offer that something in your browser hides); (since 1.12.2) your own incoming offers page
(`steamcommunity.com/…/tradeoffers/`) the same way, when you open it or the window of one of your offers, only to compare
the items each offer shows with Steam's own record of it (items painted into an offer or hidden from it); (since
1.12.10) before auto accept takes a gift, that offer's own page (`steamcommunity.com/tradeoffer/<id>/`), once per try,
only to confirm in Steam's own record of that offer that you give nothing in it. The web chat's friends and dialogs are read in
the chat page itself, with no request to Steam's servers apart from loading the avatar pictures of look-alike pairs
from Steam's picture servers (avatars.fastly.steamstatic.com or the chat page's own avatar host), as the page loads them, without cookies or referrer. The
background part asks Steam's public store API (`store.steampowered.com/api/appdetails`, `/api/packagedetails`) for
prices and pictures of games and packages without your cookies, and, for the inventory check only, reads your own
inventory (`steamcommunity.com/inventory/…`, nothing else) with your Steam cookies, so that no script of the page can
see or change the answer: the browser adds the cookies itself; the background part neither reads nor keeps them,
follows no redirect and sends them to no other address. The extension's background part also reads your sent trade
offers page (since 1.12.1) and your incoming trade offers page (since 1.12.2) on steamcommunity.com and, before auto
accept takes a gift, that offer's own page `steamcommunity.com/tradeoffer/<id>/` (since 1.12.10), once per try (those
addresses, no other), the same way, only to compare them with what the page shows — of an offer's own page the page
gets only Steam's record of that offer (its items' numbers, the partner's account id (SteamID64), the offer id and the
trade hold days the page names: what the page already shows), never the page itself; for a gift auto accept takes,
this one read also stands in for the page's own read of that offer's page; nothing is stored. (Since 1.12.1)
The inventory value next to the wallet balance reads your own inventories (TF2, CS2, Dota 2, Steam; Rust when your
price source prices it) from Steam with the page's own requests, from one tab, on a click on Σ or, set to
"Automatic", by itself every 30 minutes, never while a trade is being accepted or sent. Item pictures come from
Steam's image servers. (Since 1.21.23) While a currency other than the US dollar is in use (your wallet's, or the one
chosen in "Show prices in"), Steam's own exchange rate is read from the Community Market: the order book of one
reference item (the TF2 key, else the Sack of Gems, else a CS2 case) in US dollars and in each such currency
(`steamcommunity.com/market/itemordershistogram`, with your Steam session, as the item's market page asks for it),
in the background about once a day for the whole browser, at most a few times a day after a failure (the wait doubles
up to a day), and the reference item's market page only when its known id has no order book; marketdb.info's daily
rates (section 5) stand in until then. (Since 1.21.23) With Steam's classic market pages on, a CS2 market page Steam
opens by a group's address asks Steam once, without your cookies, for that item's listings
(`steamcommunity.com/market/actions?q=QueryListingsForItem`), only to find its name for the classic search page.
(Since 1.21.15) An item's order book in another currency than your wallet's is one more request to Steam's own order
book in that currency, when you pick it. The item counts in Steam's header (keys, tickets and gem sacks by default) are
read from your own inventory (Steam's inventory endpoint, with your Steam session) at most every 15 minutes by one tab
and when you open your inventory page, and (since 1.21.23) once about 20 seconds after a trade Smart Trader sees
(several trades close together: one read; for a trade accepted elsewhere, one list of your incoming offers and one
request per trade for its items, three at most).

### 5. Optional services
The optional third-party services and sites are all under one box (since 1.21.24, as from 1.18.0 to 1.21.22; in 1.21.23 the sites for prices and pictures had no box and were asked of the browser by "I agree", and a box of their own turned on the services that receive Steam IDs): "Use the optional third-party services and sites" on the page shown before Smart Trader starts, "Allow the optional services and sites" in the extension's options (the same box).
Under it: the price sources (since 2026-10-09) marketdb.info, pricempire and the marketplaces' public price files (Market.CSGO and its TF2, Dota 2 and Rust sites, Waxpeer, LOOT.FARM, Lis-Skins), the KEYS.LAND Telegram channel and (since 1.21.23) itempedia.tf's pictures of TF2 Unusual effects, which receive nothing about you or your items; the three reputation sites (backpack.tf, SteamTrades, CSGO-Rep), which receive the public SteamID64 of a trade partner you look at; and (since 1.18.0) steamapis.com, which receives your own key and the SteamID64 of each inventory loaded through it.
The box is empty on the first run, and "I agree to the License Agreement and the data notice" then accepts the agreement and the data notice only: nothing is asked of the browser and none of these services runs. Ticked, the same button also asks the browser, in one prompt, to allow all of their sites, and the box counts as ticked only once the browser holds every one of them; if you decline that prompt, your agreement is still recorded and these services stay off until you tick the box in the options. When the page asks again after an update, the box is ticked as you left it while the browser still allows every one of those sites, or when the browser cannot tell (then "I agree", with the box left as it is, keeps your services as they were: nothing is asked, turned off or given back); when one of those sites is no longer allowed, the box is empty and a line under it says that you had it ticked — tick it again and the same button asks the browser for them.
Unticking it — on that page when it asks again, or in the options — turns every one of them off and gives their sites' access back to the browser; the browser's own site access settings for the extension, or "Delete all Smart Trader data", take a site's permission back as well.
While the box is not ticked, prices come from the Steam Market only, with no Unusual effect pictures, no marketplace prices, no KEYS.LAND fallback and no partner reputation from these sites; Smart Trader's settings on Steam show a red notice with a button to the options, and its button in Steam's header blinks red.
Smart Trader's default settings use marketdb.info prices and Waxpeer's price file (the factory Preset 1), KEYS.LAND's Telegram fallback (when the keys.land relay does not answer), the pictures of TF2 Unusual effects from itempedia.tf and the reputation sites, so ticking the box starts them right away: the partner reputation from backpack.tf (with its tools on backpack.tf pages), SteamTrades (with your steamtrades.com cookies) and CSGO-Rep.
pricempire is asked only once you enter your own API key, the other marketplaces' price files only once you choose them.
steamapis.com is never used by default: only once you choose it as the source of big inventories in the settings and save your own key on the options page.
The lists on that page name each one with its sites, what it receives and when it is asked.
Each one is still asked only while its own setting in Smart Trader uses it: a price source only while it is the price source in its settings
(marketdb.info also while a marketplace is: its exchange rates convert their US dollar prices, and its price lists value
the items the marketplace does not price when "Items the marketplace does not price" is set to "marketdb.info after
Steam's fee and the cash-out fee"). marketdb.info is Smart Trader's default price source (since 1.12.2): until the box is ticked (and the browser allows its site), Smart Trader takes its prices from the Steam Market instead. Since 1.14.0 Smart Trader can use several price sources at once, in order
(price presets, on by default): a source is then asked only while it is a member of the active preset and an item
reaches it — the source above it has no price of that item (the factory Preset 1 is KEYS.LAND → marketdb.info → Steam
Market → Waxpeer: Waxpeer's price file only for CS2, Dota 2 and Rust items the Steam Market has no listing for, and only while the box is ticked). Since 1.21.21 a trade window also loads ahead of time marketdb.info's price lists of the other
games present in either side's inventory (the setting "marketdb.info: load the lists of"; from idle time, the open
tabs first): the same request as above, only the game id and the time window. They receive nothing
about you or your items: the game, the time window or the marketplace of a whole price list, and pricempire also your
own API key. pricempire works only with your own key from your pricempire account: you set it on the extension's
options page (since 1.21.9; a key entered before in Smart Trader's settings is moved there once), it is kept in the
extension's own database on this computer apart from the settings, and the extension's background part sends it only to
`api.pricempire.com`, as the `Authorization` header of its requests, never in an address and never to any other host;
it is never handed to a web page, Steam's included, and never written to the diagnostic log. The keys.land price relay is allowed from the start (its host is installed with the
extension), and Smart Trader asks it only while its prices are on in Smart Trader's settings (KEYS.LAND → "Use
KEYS.LAND prices", on from the start since 1.12.2; the KEYS.LAND prices switch turns it off; since 1.12.4 the one switch
of those prices with any price source, a marketplace included), or, for its Steam conversion figures only, while a
marketplace is the price source and the items it does not price are valued less the automatic cash-out fee, or while
Steam Market or marketdb.info prices are shown as cash ("Cash after the cash-out fee", on by default; always while
KEYS.LAND is on); it receives nothing about you. The KEYS.LAND Telegram channel (since 1.17.0) is the fallback of
those prices: it is under the one box (since 1.21.24, as from 1.18.0 to 1.21.22; in 1.21.23 one of the sites for prices and pictures, with no box; in 1.17.0 it had a box of its own, unticked until you ticked it), and Smart Trader reads its one public page only when the keys.land relay did not answer and
"Use KEYS.LAND prices" and its own setting (KEYS.LAND → "When
keys.land cannot be reached, take its prices from its public Telegram channel") are on — at most once in 30 minutes (once a minute while no KEYS.LAND prices are at hand) for
all your tabs together; Telegram receives nothing about you. You can untick the box in the options at any time (every one of them stops), take a site's permission back in the browser's own site access settings for the extension, and turn each one off alone by its own setting in Smart Trader. None of them receives cookies from the extension, except SteamTrades: the SteamTrades request carries your own
steamtrades.com cookies, so the site answers as it would in your own tab (it is needed to pass its bot check); this
happens only while SteamTrades is turned on, only on that one request, and the form tokens of its page are removed from
the answer before Smart Trader reads it. Each of them,
like any website, sees your IP address, your browser's name and version (User-Agent) and the time of the request.

steamapis.com (since 1.18.0) is under the same box, and it is never used by default: it works only
with your own steamapis.com API key, which you set on the extension's options page, and only once you choose it as the
source of big inventories in Smart Trader's settings (off by default). Smart Trader never asks for an API key on a website, in chat or in a trade. The key
is kept in the extension's storage on this computer, never handed to Steam's pages, and the extension's background part
sends it only to `api.steamapis.com`, as the `x-api-key` header of its requests, never in an address and never to any
other host. Smart Trader asks steamapis.com only when you start the load of an inventory too big for Steam's own limit
(the stacks' or card sets' "load the rest", the price list's "Load all", a bulk run, the panel's "Continue loading"),
never on its own; before the first request it tells you the cost, and before someone else's inventory goes through it,
it asks you once for that profile (a setting can allow only your own, or every profile). steamapis.com is an independent
paid service (Datagrab OÜ, Estonia); by its own policy it keeps request logs, with your IP address and the SteamIDs you
look up (including other people's), for up to 2 years.

| Service | What is sent | When |
| --- | --- | --- |
| keys.land price relay (the host listed in the extension's permissions) | only which price is wanted: `GET …/kl/v1/market/series?item=key` (or `ticket`, `gems`) `&range=24h`; and the Steam conversion figures of keys, tickets and gems: `GET …/kl/v1/steam/convert` (no parameter). Nothing about you or your account. (Since 1.22.0) The CS2 price lists our server collects from cs2.sh (the Steam Market and five marketplaces: BUFF, Youpin, CSFloat, Skinport, C5Game): `GET …/v1/cs2sh/latest?sources=<the sources>` sends only the list of sources; nothing about you or your items, never an item's name. Once a day also the marketplace ids of CS2 items for the links in the item card (`GET …/v1/cs2sh/ids`, no parameter): nothing about you. | when prices of TF2 keys, tickets or gems are shown (at most once a minute) — only while KEYS.LAND prices are on in Smart Trader's settings (on from the start since 1.12.2; the KEYS.LAND prices switch turns them off; with any price source, a marketplace included); the conversion figures only while a marketplace is the price source and the items it does not price are valued less the automatic cash-out fee, or while Steam Market or marketdb.info prices are shown as cash (on by default; always while KEYS.LAND is on) (at most every few minutes); (since 1.22.0) the CS2 price list: one list, kept 15 minutes, when a CS2 item needs a price from a cs2.sh member of your active preset ("Steam Market (cs2.sh)", "Marketplaces (cs2.sh)") or the CS2 tab's prices on the marketplaces are on and a page shows CS2 items; the ids file once a day under the same condition (kept 24 hours); the relay itself is allowed from the start and the options can turn it off |
| Telegram (`t.me`), the KEYS.LAND channel | only the request for the channel's public page: `GET https://t.me/s/keysland`. Nothing about you or your items, no cookies. Only the prices of keys, tickets and gems of its latest usable price post (of an earlier one on the page when newer ones cannot be read or their prices are far from the last known ones) and the post's time are taken from the page. | only while the one box of the optional third-party services and sites is ticked and the browser allows `t.me` (since 1.21.24, as from 1.18.0 to 1.21.22; in 1.21.23 one permission for the sites for prices and pictures, asked when you agreed to the data notice; in 1.17.0 its own box), KEYS.LAND prices and the Telegram setting are on, and the keys.land relay did not answer; at most once in 30 minutes (once a minute while no KEYS.LAND prices are at hand) |
| backpack.tf (`backpack.tf`) | the public SteamID64 of the profile or trade partner you look at: `GET https://backpack.tf/api/IGetUsers/v3?steamid=<SteamID64>` | when you open a profile, a trade offer or the trade history |
| SteamTrades (`www.steamtrades.com`) | the same SteamID64: `GET https://www.steamtrades.com/user/<SteamID64>`, with your own steamtrades.com cookies (since 2026-10-07; needed to pass its bot check) | the same |
| CSGO-Rep (`api.csgo-rep.com`) | the same SteamID64: `POST https://api.csgo-rep.com` with `{"id": <number>, "query": {"steam_id": "<SteamID64>"}}`; now and then `GET https://api.csgo-rep.com/config` (nothing about you) | the same |
| marketdb.info (`marketdb.info`) | only the game id and the time window of a whole price list: `GET https://marketdb.info/api/v1/prices?game=<game id>&hours=<24, 168 or 720>`; once a day the exchange rates: `GET https://marketdb.info/api/v1/exchange-rates` (since 1.21.23 a stand-in until Steam's own rate is read, section 4). Nothing about you or your items, never an item's name. | when prices of a game are shown and its kept list is older than a few hours — only while the service is on and marketdb.info is the price source, or a marketplace is (its exchange rates, and its price lists when "marketdb.info after Steam's fee and the cash-out fee" values the items the marketplace does not price); with price presets (since 1.14.0), while it is a member of the active preset and an item reaches it; its exchange rates also while a marketplace is a member of the active preset (the marketplace's prices shown in your wallet's currency) |
| pricempire (`api.pricempire.com`) | the game id, the marketplace and your own API key: `GET https://api.pricempire.com/v4/trader/items/prices?app_id=<game id>&sources=<marketplace>&currency=USD` (with a subscription `/v4/paid/…`), with the header `Authorization: Bearer <your key>`; now and then `GET https://api.pricempire.com/v4/free/status` (or `/limits`, `/currencies`) with the same header. Nothing else about you or your items. | when CS2 prices are shown and the kept list is older than its refresh time — only while pricempire is the price source and the service is on; with price presets (since 1.14.0), while the active preset's marketplace is priced through pricempire and an item reaches it |
| marketplace price files (`market.csgo.com`, `tf2.tm`, `market.dota2.net`, `rust.tm`, `api.waxpeer.com`, `loot.farm`, `lis-skins.com`) | only the request for the public price file of a game, for example `GET https://market.csgo.com/api/v2/prices/USD.json`, `GET https://api.waxpeer.com/v1/prices?game=csgo&minified=1`, `GET https://loot.farm/fullprice.json`, `GET https://lis-skins.com/market_export_json/csgo.json`. Nothing about you or your items, no key. | when prices of a game are shown and the kept list is older than two hours — only from the marketplace chosen as the price source, and only while the service is on; with price presets (since 1.14.0), only from the active preset's marketplace, while an item reaches it |
| steamapis.com (`api.steamapis.com`) | the SteamID64, game and context of the inventory you load and where its next page starts: `GET https://api.steamapis.com/v2/steam/users/<SteamID64>/inventory/<game>/<context>?count=2000&start_assetid=<id>`, with the header `x-api-key: <your key>`. Nothing else about you or your items. | (since 1.18.0) only while the one box of the optional third-party services and sites is ticked (in 1.21.23 the box of the services that receive Steam IDs) and steamapis.com is chosen as the source in Smart Trader's settings (off by default), when you start a load (the stacks, the card sets, the price list's "Load all", a bulk run, the panel's "Continue loading") of an inventory too big for Steam's own limit; someone else's inventory only after your confirmation for that profile (or always, if you chose so in the settings); at most your daily number of requests |

Results are kept on your computer for a few hours (section 2); the price sources' lists only as item names with
their prices and counts. The keys.land price relay is run by the author of Smart
Trader; it only forwards public price data from KEYS.LAND, an independent service whose data is used with its owner's
permission; since 1.22.0 it also hands over the CS2 price lists our own server collects from cs2.sh (an independent price service, used under its terms; the key for it lives only on our server, never in the extension), and the extension sends it only the list of sources it wants, nothing about you or your items. The relay keeps only ordinary server logs (the requested address and the time) for a short time and nothing
about your account. backpack.tf, SteamTrades, CSGO-Rep, marketdb.info, pricempire, steamapis.com, the marketplaces
and Telegram each apply their own terms and privacy policy, published on their sites.

While the one box is ticked and the browser allows backpack.tf, the extension also
runs its tools on the backpack.tf pages you open (listing prices in trade offer links, backpack totals); otherwise it
does not run there at all. On those pages only your settings, the
state of the tips and the values of the backpack.tf tools themselves are made available to the page; your saved trade
links, trade partners, offer records, reputation results, purchase history and the diagnostic log are not.

Unusual effect pictures (Smart Trader's settings → Items & inventory, on by default since 1.21.23 and turned on once
for every installation at that update): only while the one box of the optional third-party services and sites is ticked (since 1.21.24; in 1.21.23 while the browser allowed the sites for prices and pictures; the data notice names itempedia.tf since its version 15) and the setting is on, the browser loads those pictures from itempedia.tf
(`https://itempedia.tf/assets/particles/<effect number>_94x94.png`). Like any picture server, it sees your IP address,
your browser, the time, the Steam site as the referrer (under the browser's default rule only its address, such as
`https://steamcommunity.com/`, not the page's) and any cookies itempedia.tf itself has set in your browser; nothing about
you or your Steam account is sent. On a Steam page in another language Steam shows the effect's name
translated and without its number: Smart Trader then asks Steam once per translated name for the English description
of one item that shows it (the item description request of section 4, in English) and keeps that name with the
effect's number among the item descriptions on your computer (section 2).

3D view of CS2 items (Smart Trader's settings → Items & inventory, on by default): nothing is sent until you click
3D View. Your click opens the viewer you chose (3dview.cs2inspects.com by default since 1.12.8; csmarketcap.com or swap.gg from the ▾
menu) with only the item's inspect link in the address — the same link Steam shows behind "Inspect in Game…". In the
extension the viewer's page (3dview.cs2inspects.com) is shown inside a window of Smart Trader's own, as an embedded page
with that same address; the other viewers, and the userscript, open a separate window or tab. The data is the same:
only the inspect link, no cookies (the embedded page is loaded without them), no referrer. The first
time, Smart Trader asks you before it opens (you can turn that question off). Since 2026 that link encodes the item
itself: type, finish, pattern seed, wear (float), stickers and charms with their positions and wear, a StatTrak™ count,
a name tag's text and the asset id, and it may carry the owner's account number; an older link instead holds the
owner's SteamID64 (or the market listing id), the asset id and a check number. No cookies, Steam session, token or
trade link go with it; the tab opens without a referrer. The viewer sees your IP address, browser and time, and may
pass the link on to its own services (for example, its 3D renderer); its own terms and privacy policy apply. The Details panel decodes the link on your computer and sends nothing.

cs2.sh (since 1.22.0; CS2 tab → cs2.sh, on by default) is opened only by your click, as an ordinary link: the "check at cs2.sh" button in the inventory (your own or another account's, while its CS2 inventory is shown) and in the trade window (while the partner's CS2 inventory tab is shown) opens that inventory's page on cs2.sh in a new tab, with the account's public SteamID64 in the address (your own, the profile's or the trade partner's); "View in cs2.sh" under Steam's "View in Community Market" in an item's menu opens the item's page there, with the item's market name in the address. Nothing is sent before the click; Smart Trader itself makes no request to cs2.sh (the CS2 price lists of section 5 come from our own server). The tab opens without an opener or a referrer, with no cookies, Steam session or token; cs2.sh sees your IP address, browser and time, and its own terms and privacy policy apply.

Links to other sites (for example SteamDB, backpack.tf, SteamTrades, Steam Card Exchange) are ordinary links: those
sites receive nothing unless you open the link.

### 6. Diagnostic log
The diagnostic log (`dev.log`) is off unless you turn it on (Smart Trader's settings on a Steam page → General →
Diagnostics). While it is on, it keeps on your computer only what is needed to find faults and slowness: timings,
counts, error messages (scrubbed) and the status of network requests, for at most 7 days and 4 MB. The file you
download also names your browser and its version, operating system, screen size class and pixel density, interface language and time
zone offset, the extension or script engine that runs it and its version, Smart Trader's versions on this installation
and when it was first installed, your settings as set (text settings by key only, never their value), the state of its
tips and a random code of this installation that tells its logs apart from another installation's. For each page view
it notes the kind of Steam page and of the page you came from (fixed words such as "inventory", never an address), a
random code of the browser tab and how the page was opened; what you do in Smart Trader's tools is recorded as fixed
words (which button or setting), never what you typed. It also records every click you make on Steam's own pages, only
as fixed words: what kind of control it was (a button, a link or a box) and where on the page, the kind of page a link
leads to, and whether you or Smart Trader clicked; Steam's answers to your declines, cancels and reports of trade offers
and to your market sales, removed listings, purchases and buy orders (which action, the answer's status and how long it
took); and which known extensions or userscripts that can conflict with it (other Steam trading tools) were found on the
page, by their fixed names. It never records
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
acceptance of the License Agreement), gives the optional services' site access back to the browser and (since 1.21.24)
deletes Smart Trader's databases in the Steam sites' own IndexedDB — the bigger caches of section 2 (`ct-cache`), the
price sources' lists (`ct-prices`) and the selling tools' price caches — on steamcommunity.com and
store.steampowered.com: through an open Steam tab or, with none open, one it opens in the background for a moment and
closes again (checkout.steampowered.com only through a tab open there). The options page says where it was done; a
site it could not finish is named, and pressing the button again with a page of that site open finishes it. What stays
after it, until you clear those sites' data in the browser: a few small switches in the Steam sites' `localStorage`
(the light theme's styles, the blurs for streams, the selling tools' cache counter, the settings tabs whose "Advanced
settings" block you left open) and the two Steam preference cookies of section 2 (`bMarketOptOut`, `birthtime`). Removing the extension removes its own storage as well, but it
does not reach the Steam sites' storage: to delete the caches there too, press "Delete all Smart Trader data" first (or
clear steamcommunity.com's and store.steampowered.com's data in the browser). Caches expire and are trimmed on their
own. The box of the optional third-party services and sites (section 5) deletes nothing: unticking it stops all of them
and gives their sites' access back to the browser at once; what they returned before stays in the caches until it
expires or you delete it.

### 9. Changes
When what the extension does with data changes, this policy is updated and the change is listed below with its date.
When a change brings a new kind of data, a new recipient or a new read with your Steam session, or corrects what this
policy told you, the effective date above changes and the extension shows its data notice again and waits for your
agreement before doing anything; a change listed with "no new kind of data, recipient or permission" keeps the
effective date and the notice you agreed to.

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
price source (section 5): this update turns KEYS.LAND on once for every installation (the KEYS.LAND prices switch turns
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
cash, KEYS.LAND on or off — the same anonymous request as before, never for the market price or the Steam balance. 2026-10-16 (1.12.10) — auto accept's gifts confirmed by each offer's own page (section 4): before auto accept takes a
gift, the background part reads that offer's own page (`steamcommunity.com/tradeoffer/<id>/`, the same site and session
as before) instead of the whole incoming offers page, and hands the page only Steam's record of that offer (its items'
numbers, the partner's account id, the offer id, the trade hold days); no new kind of data, recipient or permission,
nothing stored. 2026-10-16 (1.12.14) — the 3D view of CS2 items inside a Smart Trader window (section 5): in the
extension the 3D button shows 3dview.cs2inspects.com embedded in a window of the extension's own (one window, reused for
the next item) instead of a new tab; the embedded page gets the same address (only the item's inspect link), is loaded
without your cookies and without a referrer, and the extension exchanges nothing with it. The other viewers still open in
a tab, the userscript opens a separate pop-up window, and "Where the 3D button shows the viewer" in the settings brings
the tab back. No new kind of data, recipient or permission. 2026-10-16 (1.14.0) — price presets (section 5): several
price sources at once, in order; each optional source is still asked only once its box is ticked, and then only while it
is a member of the active preset and an item reaches it (the source above it has no price of it); Waxpeer is in the
factory Preset 1 for CS2, Dota 2 and Rust items the Steam Market has no listing for. No new kind of data, recipient or
permission. 2026-10-16 (1.15.1) — corrections after a check of this policy against the code, no new behaviour: the table
of section 5 says when each price source is asked with price presets; section 6 names what the diagnostic log's
file holds more fully (also each page view's kind of page and tab code, what you do in the tools and every click on
Steam's own pages as fixed words, Steam's answers to your trade and market actions, and the conflicting extensions or
scripts found); section 9
says when the data notice is shown again. The License Agreement is re-issued as version 2026-10-16 (its section 8: a
price service is asked only while your price settings use it; the 3D viewers as they open now). Because these words
changed, the extension shows its data notice again (its version 11). 2026-10-16 (1.15.2) — skinflow.gg removed from
the 3D viewers (section 5): it is the same service as 3dview.cs2inspects.com; the 3D button now opens
3dview.cs2inspects.com (the default), csmarketcap.com or swap.gg, and a viewer chosen as skinflow.gg becomes
3dview.cs2inspects.com once. The License Agreement's section 8 no longer names it. No new kind of data, recipient or
permission. 2026-10-17 (1.16.1) — the partner history of the
Phishing and scam protection (section 2): how many trades you had with each partner and the days of the first and last
one, as one-way keyed hashes of the partner's SteamID with counts and days only (and, to count each trade once,
keyed hashes of the newest 4,000 trades with their days), built on your computer from the trade
history pages you open, the offers you accept and the accepted sent offers the offer watch already reads (no new
request, nothing sent), shown as a hint on the offers pages and in the trade window; "Forget partner history" deletes
it. Because this is a new kind of data kept on your computer, the effective date changes and the extension shows its
data notice again (its version 12). The same release adds a security alert when Steam signs you out in this browser,
told by the offer watch's own check (one alert per sign-out, only the account's keyed hash and the time kept to say it
once): no new kind of data, recipient or read. 2026-10-17 (1.17.0) — the KEYS.LAND Telegram channel as the fallback
of the keys.land prices (sections 2 and 5): when the keys.land relay does not answer, Smart Trader may read the
channel's public page `https://t.me/s/keysland` (at most once in 30 minutes, without cookies) and take the prices of
keys, tickets and gems from its latest usable price post — from an earlier one on the page when newer ones cannot be read or their prices are far from the last known ones; it keeps
them on your computer (six prices and the post's number and time). Telegram is a new recipient (it sees your IP
address, browser and the time of that request), so the effective date changes and the extension shows its data notice
again (its version 13); the service is off until you tick its box. 2026-10-17 (1.18.0) — one box for all the optional
third-party services and sites (section 5): "Third-party services and sites" takes the place of a box per
service on the data notice page and a switch per service in the options; ticking it allows all of them at once (the
browser asks once for all of their sites), unticking it turns all of them off and gives their sites back to the
browser, and the list under it names each one with its sites, what it receives and when it is asked. Each one is still
asked only while its own setting in Smart Trader uses it. Under that box, a new optional service, steamapis.com (sections 2 and 5): big inventories loaded with your own
steamapis.com key, set only on the extension's options page and sent only to api.steamapis.com; a new recipient of the
SteamID64 of the inventories you load through it, your own and other people's (after your confirmation for that
profile, or always if you chose so in the settings); never used by default — asked only when you choose it as the
source of big inventories in the settings and start such a load. Because of that new recipient, because the choice is
now one for all of them (an earlier choice of single services does not carry over) and because the License Agreement
is re-issued as version 2026-10-17 (its section 8), the extension shows its data notice again (its version 14) with
the box unticked. 2026-10-17 (1.19.2) — the Phishing and scam protection (section 2) is an experimental feature and off
by default: nothing of its item in section 2 is read or kept until you turn its tab on in Smart Trader's settings; an
installation that never changed a setting of that tab is switched off once at the update, one that did keeps its
choice. The trade items check's own guard of auto accept (a gift accepted only once Steam's record of the offer confirms
it: the read of that offer's page described in section 4) stays whatever the tab's switch says. No new kind of data,
recipient or read; the policy's text only says less is read by default. 2026-10-18 (1.21.2) — the trade items check's
guard of auto accept follows the Phishing and scam protection's tab like every other check of it: with the tab off,
the gift's offer page (section 4) is not read and auto accept takes a gift without Steam's record confirming it. No
new kind of data, recipient or read; the effective date is unchanged. 2026-10-24 (1.21.21) — a trade window loads
ahead of time marketdb.info's price lists of the other games present in either side's inventory (section 5; the
setting "marketdb.info: load the lists of", from idle time): the same request as before, only the game id and the time
window; a price of too few sales is final by default and no longer sends the item on to the next source, and price
floors spare the next source an item already known to be cheap. No new kind of data, recipient or permission; the
effective date is unchanged. 2026-10-24 (1.21.23) — the Unusual effect pictures from itempedia.tf (section 5) are on by default and, in the extension, among the sites for prices and pictures (the data notice names itempedia.tf among them): only the effect's number in the picture's address, as before; on a Steam page in another
language the effect's English name is asked of Steam once per translated name (the item description request of
section 4) and kept with the item descriptions (section 2). The setting is turned on once for every installation at
this update (a later change of yours is kept). In the same version the extension's consent became one step (section 5): the sites for prices and pictures, which
receive nothing about you (marketdb.info, pricempire, the marketplaces' price files, the KEYS.LAND Telegram channel,
itempedia.tf), have no box any more — their sites are asked of the browser when you press "I agree to the License
Agreement and the data notice" (one prompt; declined, they stay off until you allow them in the options); the one box
left is for the services that receive Steam IDs (backpack.tf, SteamTrades, CSGO-Rep, steamapis.com), unticked on a
first run and ticked as you left it when the notice is shown again; the automatic acceptance of gift offers is asked
when you turn it on, no longer on that page. Because itempedia.tf is now named among those sites and the pictures start
for every installation, the effective date changes and the extension shows its data notice again (its version 15); no
new kind of data. The License Agreement shown with it is re-issued as version 2026-10-24: its opening, section 2 and
section 8 describe this one step; its section on automation is unchanged, so a consent to automation given under
2026-10-17 is kept. 2026-10-25 (1.21.24) — corrections after a check of this policy against the code of 1.21.23 and
the CS2 tiles of 1.21.24, and one change: section 4 names the English description of a TF2 or CS2 item class the tools
ask Steam for on a Steam page in a language other than English (since 1.21.23; at most 200 a page visit, kept with the
item descriptions), Steam's own exchange rate read from the Community Market's order book of one reference item with
your Steam session (since 1.21.23; marketdb.info's rates only a stand-in until then), the one read without your
cookies of a CS2 market page Steam opens by a group's address (since 1.21.23), the order book of an item in another
currency than your wallet's (since 1.21.15) and the reads of the item counts in Steam's header (once more after a
trade since 1.21.23); section 2 names the rates and the ids of your sent offers awaiting your confirmation kept for
the header's blinking button (since 1.21.23), the Fear & Greed index's order-book history (since 1.21.18), two of
Steam's own preference cookies that two settings write (bMarketOptOut, birthtime) and that since 1.21.0 the bigger
caches are kept in the Steam sites' own IndexedDB, which "Delete all Smart Trader data" did not reach before this
version. The change (section 8): "Delete all Smart Trader data" now deletes those databases too, through an open Steam
tab or one it opens in the background for a moment; what stays after it is a few small switches in the sites'
`localStorage` and the two cookies, and removing the extension still does not reach the Steam sites' storage. Section
5 calls the 3D button by its new name, "3D View". The CS2 tiles' new look and the float scale of 1.21.24 only show
Steam's own item data from the page: no new kind of data, recipient or read. In the same version the extension's consent is one box again (section 5, the owner's decision of 2026-10-25): every optional third-party service and site — the sites for prices and pictures and the services that receive Steam IDs alike — is under one box, "Use the optional third-party services and sites", empty on a first run; "I agree to the License Agreement and the data notice" then accepts the agreement and the notice only, and with the box ticked it asks the browser for all of their sites in one prompt; when the notice is shown again the box is ticked as you left it while the browser still allows every one of them, and unticking it there or in the options stops all of them and gives their sites' access back to the browser. While it is not ticked, Smart Trader's settings on Steam show a red notice and its button in Steam's header blinks red. No new kind of data or recipient. The License Agreement shown with it is re-issued as version 2026-10-25: its section 8 describes this one box; its section on automation is unchanged, so a consent to automation given under 2026-10-17 or 2026-10-24 is kept. Because these words correct what this
policy told you, the effective date changes and the extension shows its data notice again (its version 16).
2026-10-31 (1.22.0) — a new read with your Steam session, and
corrections of what this policy told you. The new read (section 4): while the sales notifications are on (Notifications
→ "Sales on the Steam Market", off unless you turn them on), one tab of the browser reads your own Steam Market history
with your Steam session once per the period you chose, for the newest sales of your own listings; nothing is sent to
anyone. Section 2 names what is kept for them: one record for the browser's account under its SteamID — the newest
sales not told yet (the item's market name, what the buyer paid and what you received with the currency's id, the
sale's time — for the newest 12; older ones only as their count and the totals per currency), the time of the newest
event of your market history with the ids of that second's sales, and the times of the last read and the last
notification; nothing about the buyer; "Delete all Smart Trader data" deletes it. The corrections (section 2): records
kept on your computer that this policy did not name before — the trades on hold the item counts in Steam's header wait
for (the offer's id, the hold's end, the inventories its items come into; 50 at most, each until a day after its hold
ends) with the time of the newest trade seen on your own trade history or offers pages; Quick accept's pace
(milliseconds per item of its clean accepts of 20 items or more, the last 10 per game, numbers only); the diagnostic
line of the extension's options page about your answer to the data notice (its version and time, the optional
services' state, the extension's id) with counts kept only in the browser's memory; and, in the Steam sites'
`localStorage`, which settings tabs' "Advanced settings" block you left open (section 8: it stays after "Delete all
Smart Trader data"). Section 5 says how the box of the optional services comes back when the notice is shown again:
ticked as you left it while the browser still allows every one of their sites or cannot tell, empty with a line under
it when one of them is no longer allowed; the License Agreement's section 8 says the same (its version 2026-10-25 is
kept, so a consent to automation is kept too). Section 1 now says exactly what is stored before you agree: only the
installation's own service state, with no personal data. Sections 2 and 5 also name, from 1.22.0, the CS2 price lists our server collects from cs2.sh (the Steam Market and five marketplaces) and hands over through the keys.land relay already listed — only the list of sources is sent, nothing about you or your items; one list kept 15 minutes — and cs2.sh among the sites only your click opens (the inventory's SteamID64 or the item's name in the address, nothing before the click). No new recipient or permission; your choice about the optional
services, the keys.land relay's switch and your consent to automation stay as they were. Because this is a new read
with your Steam session and these words correct what this policy told you, the effective date changes and the
extension shows its data notice again, once (its version 17).

### 10. Contact
ggggggdev@gmail.com

Smart Trader is an independent project. It is not affiliated with, endorsed or sponsored by Valve Corporation. Steam
and the Steam logo are trademarks and/or registered trademarks of Valve Corporation in the U.S. and/or other countries.

---

## Українська

**Діє з:** 2026-10-31 · **Контакт:** ggggggdev@gmail.com

Smart Trader додає інструменти для обміну на сторінки Steam: зведення пропозицій обміну й ціни предметів, швидше
прийняття вибраних вами пропозицій, помічники для інвентарю й торговельного майданчика, підсумки історії обмінів,
перевірку репутації партнерів, попередження про фішинг і скам і сповіщення на робочому столі. Ця політика описує
всі дані, з якими працює розширення, куди вони йдуть і як їх видалити. Вона відповідає коду розширення; якщо код
почне інакше поводитися з даними, зміниться і ця політика, і повідомлення в розширенні, а розширення знову попросить
вашої згоди, перш ніж щось робити.

### 1. Нічого не відбувається без вашої згоди
Після встановлення розширення показує повідомлення про дані. Доки ви не натиснете «Погоджуюсь», нічого не працює
на сторінках Steam і запитів немає; зберігається лише службовий стан встановлення (які додаткові сервіси ввімкнено,
лічильники діагностики), без особистих даних.

### 2. Дані на вашому комп’ютері
Зберігаються у вашому браузері на цьому комп’ютері — у сховищі розширення (`chrome.storage.local`), а з 1.21.0 більші
кеші — у власній IndexedDB сайтів Steam (див. після цього списку) — і нікому не надсилаються, зокрема й нам:
- ваші налаштування Smart Trader і стан його панелей і турів;
- мітки предметів і нотатки, які інструменти ведуть про предмети;
- збережені вами посилання для обміну (вони містять токен посилання партнера, а після прочитання — нікнейм партнера й
  адресу його аватара) і ваше власне посилання (з вашим нікнеймом і адресою аватара);
- підсумки й кеші з відкритих вами сторінок: підсумки історії обмінів та інвентарю, описи предметів, ціни
  торговельного майданчика, результати перевірки репутації, списки друзів, записи прийнятих вами пропозицій (з нікнеймом
  партнера), історія кошика магазину; ціни ключів, білетів і гемів, востаннє прочитані з Telegram-каналу KEYS.LAND
  (шість цін, номер і час поста, коли сторінку прочитано і чому останнє читання не вдалося, якщо так: не довше тижня);
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
- чи можуть працювати інструменти на сторінках backpack.tf: одне «так / ні», яке код Smart Trader на сторінках Steam
  копіює з налаштувань («Сторінки backpack.tf» і перемикач гри «Team Fortress 2»), щоб фонова частина розширення
  завантажувала ці інструменти на backpack.tf лише поки ввімкнено обидва;
- ваш API-ключ pricempire, якщо ви задасте його на сторінці параметрів розширення (ніколи на сайті; з 1.21.9, раніше —
  у налаштуваннях Smart Trader): зберігається у власному сховищі розширення окремо від налаштувань (його власна база
  даних, яку не може прочитати жодна вебсторінка й жодна частина розширення, що працює на сторінці), ніколи не
  передається сторінкам Steam, фонова частина розширення надсилає його лише до pricempire (розділ 5);
- (з 1.18.0) ваш API-ключ steamapis.com, якщо ви задасте його на сторінці параметрів розширення (ніколи на сайті):
  зберігається у власному сховищі розширення окремо від налаштувань (його власна база даних, яку не може прочитати жодна вебсторінка й жодна частина розширення, що працює на сторінці), ніколи не передається сторінкам Steam, фонова
  частина розширення надсилає його лише до steamapis.com (розділ 5); і, лише в цьому браузері, скільки запитів пройшло
  через нього (цього місяця, сьогодні) та їхній звичайний час;
- (з 1.12.0) те, що потрібно Захисту від фішингу та скаму (окрема вкладка в налаштуваннях Smart Trader; з 1.19.2 —
  експериментальна функція, типово вимкнена: ніщо з цього пункту не читається й не зберігається, доки ви не ввімкнете
  одну з її перевірок; з 1.22.0 кожна перевірка — власний перемикач), щоб помітити зміну, — лише як односторонні ключовані хеші (відбитки, зроблені на цьому комп’ютері з
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
  Якщо стеження за трейдами вимкнено, захист тримає фонове стеження за трейдами для своєї перевірки трейдів, з його
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
- (з 1.21.23) власні курси Steam для валют у вжитку (вашого гаманця й вибраної в «Показувати ціни у валюті»): кожен
  курс із часом читання, ринковий ідентифікатор еталонного предмета, з якого його прочитано, а після невдалого читання —
  його час і скільки невдач було поспіль — нічого про вас; курс використовується щонайбільше тиждень, «Очистити кеш цін»
  (Загальні → Інструменти) видаляє їх;
- (з 1.21.23) для кнопки, що блимає в шапці Steam, для кожного акаунта під його SteamID: ідентифікатори ваших
  надісланих трейдів, що чекають на підтвердження в мобільному застосунку Steam або поштою (щонайбільше 100, кожен
  щонайбільше 15 днів), і час трейдів, надісланих із цього браузера за останню годину (щонайбільше 20); видаляються,
  поки налаштування цієї кнопки вимкнене;
- (з 1.22.0) для кількостей предметів у шапці Steam, для кожного акаунта під його SteamID (щонайбільше три акаунти):
  крім кількості в кожному інвентарі й часу, коли її прочитано, — трейди на утриманні, предметів яких чекають ці
  кількості (id трейд-оферу, коли Steam завершує утримання і в які з ваших інвентарів — номери гри й контексту —
  надійдуть його предмети; щонайбільше 50, кожен до доби після кінця утримання), і час найновішого трейду, побаченого
  на ваших власних сторінках історії трейдів або трейд-оферів — лише кількості, ідентифікатори й час, без назв
  предметів;
- (з 1.22.0) темп Quick accept: скільки мілісекунд на предмет Steam витратив на чисті прийняття 20 предметів і більше
  в цьому браузері (останні 10 для кожної гри й для всіх ігор), для його зворотного відліку й довших очікувань, поки
  Steam повільний, — лише числа, без трейдів і без акаунта;
- (з 1.22.0) коли сповіщення про продажі на вкладці «Сповіщення» ввімкнено («Продажі на Ринку Steam», вимкнено, доки
  ви їх не ввімкнете), один запис для акаунта цього браузера, під його SteamID (вхід в інший акаунт починає його
  заново, нічого не повідомляючи про попередній): найновіші продажі ваших власних лотів на Ринку Steam, які цей браузер
  побачив і про які ще не сповістив (ринкова назва предмета, скільки заплатив покупець і скільки отримали ви з id
  валюти Steam, час продажу — для 12 найновіших; для старіших лише їхня кількість і загальні суми за кожною валютою, з
  часом найдавнішого з них), час найновішої події вашої історії Ринку (виставлення чи зняття лота, покупка, продаж) з
  id лотів і покупок Steam лише продажів цієї секунди (щоб рахувати кожен продаж один раз) і
  час останнього читання вашої історії Ринку та останнього сповіщення — для одного сповіщення за період; нічого про
  покупця; коли ви вимикаєте сповіщення, запис лишається як є, «Видалити всі дані Smart Trader» видаляє його;
- (з 1.16.1) скільки трейдів у вас було з кожним торговим партнером і дні першого й останнього з них — лише як
  односторонні ключові хеші SteamID партнера з кількостями й днями (без імен, без предметів), для кожного акаунта
  (щонайбільше п’ять, по 2 000 партнерів), разом із ключовими хешами 4 000 найновіших трейдів (id трейд-оферу або
  партнера з хвилиною трейду) і їхніми днями, щоб рахувати кожен трейд один раз, і тим, наскільки прочитано історію
  трейдів, зібрані зі сторінок історії трейдів, які ви відкриваєте, трейдів, які ви приймаєте, і ваших надісланих трейдів, які стеження за трейдами читає прийнятими; Захист від фішингу та скаму показує
  «Жодного трейду з <дата>» на трейді від партнера, якого в ній немає. Нічого нікуди не надсилається; «Забути історію
  партнерів» (налаштування Smart Trader → Захист від фішингу та скаму) видаляє її;
- ваша відповідь на повідомлення про дані й ваше прийняття Ліцензійної угоди: лише її версія, час і ваш вибір щодо
  автоматизації (автоприйняття, автоскасування), без даних акаунта; (з 1.22.0) сторінка параметрів розширення (Огляд)
  показує їх у рядку діагностики під повідомленням про дані разом зі станом додаткових сервісів та id розширення, а
  також лічильники, що зберігаються лише в пам’яті браузера, доки його не закрито: скільки разів від запуску браузера
  показано повідомлення й чому та скільки читань сховища розширення не вдалося.

З 1.21.0 більші з цих записів зберігаються не в сховищі розширення, а у власній IndexedDB сайтів Steam у вашому
браузері (база даних `ct-cache` сайту steamcommunity.com, а також store.steampowered.com, коли сторінки магазину
користуються цими кешами): описи предметів (на сторінці Steam не англійською — разом з англійськими описами з розділу
4: там щонайбільше 20 000 класів предметів, інакше 5 000; англійський опис запитується знову через 30 днів), ціни
Торгового майданчика спільноти й ціни книг заявок, набори карток і рівні значків, предмети надісланих вами трейдів,
історія партнерів, журнал часу Quick accept (ідентифікатори трейдів лише як короткі коди), назви предметів, які
пропонують налаштування шапки, і (з 1.21.18) історія книги заявок кожної відкритої вами сторінки предмета для індексу
страху й жадібності (час, кількість лотів і заявок на купівлю, спред та індекс: рядок на годину за 7 днів, рядок на
день до того, щонайбільше 30 днів і 500 предметів). Нічого з цього нікуди не надсилається. «Очистити кеш предметів»
(описи, набори карток і рівні, запропоновані назви) й «Очистити кеш цін» (ціни та історія індексу страху й жадібності)
у налаштуваннях Smart Trader → Загальні → Інструменти, а також «Забути історію партнерів» їх видаляють; з 1.21.24
«Видалити всі дані Smart Trader» на сторінці параметрів розширення теж видаляє цю базу — разом з іншими базами даних
Smart Trader на сайтах Steam (розділ 8).

Кілька функцій сторінок також тримають невеликі значення у власному сховищі сайту Steam у вашому браузері
(`localStorage` та IndexedDB сайтів steamcommunity.com чи store.steampowered.com, як-от кеш цін ринку для
інструментів продажу та списки цін увімкнених вами джерел цін: назви предметів із цінами й кількостями, нічого про
вас; з 1.22.0 також один список цін CS2 (Ринок Steam і п’ять маркетплейсів), який сервер цін keys.land передає з cs2.sh, зберігається типово 15 хвилин («Список cs2.sh: питати знову через» на вкладці CS2), назви предметів із цінами й кількостями й нічого про вас, видаляється кнопкою «Очистити» на вкладці «Провайдери цін»; також ідентифікатори предметів CS2 на маркетплейсах (Buff, Youpin, C5GAME) для посилань у картці предмета, один файл із того ж сервера, зберігається 24 години, нічого про вас, видаляється тією ж кнопкою «Очистити»; з 1.12.1, поки ввімкнено розмиття для стрімів, — котре з трьох увімкнено: гаманець, імена, аватари, щоб воно
діяло з першого кадру сторінки; з 1.22.0 — у яких вкладках налаштувань ви залишили розгорнутим блок «Додаткові
налаштування»), як це роблять і самі сторінки Steam. З 1.21.24 «Видалити всі дані Smart Trader»
видаляє й ці бази IndexedDB (розділ 8); кілька значень у `localStorage` лишаються, доки ви не очистите дані цього
сайту в браузері. Два налаштування також записують по одному власному cookie налаштувань Steam, як це роблять кнопки
самого Steam: «Завантажувати класичні сторінки ринку Steam замість Market Beta» (Продаж і ринок; з 1.21.18 типово
ввімкнене для нових установлень) записує `bMarketOptOut` на steamcommunity.com/market — значення власної кнопки Steam
«Exit Market Beta», щоб Steam віддавав класичні сторінки ринку там, де вони ще є; коли налаштування вимкнено,
розширення видаляє записаний ним cookie, — а «Пропускати перевірку віку в магазині» (Магазин Steam, типово ввімкнене)
записує `birthtime` на store.steampowered.com — сталу дату народження (1 січня 1980 року), яка відповідає на перевірку
віку магазину. Steam читає їх разом зі своїми сторінками; у них немає нічого про вас, і нікуди більше вони не
надсилаються.

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
ціни, стан пропозицій) з вашою сесією Steam, як це зробила б сторінка. (З 1.21.23) На сторінці Steam мовою, іншою за англійську,
вони також просять у Steam англійський опис класу предмета TF2 чи CS2, рядки якого не можуть прочитати цією мовою
(щонайбільше 200 за відвідування сторінки, у фоні; зберігається разом з описами предметів розділу 2 і запитується
знову через 30 днів); це йде лише до Steam. (З 1.22.0) Поки сповіщення про продажі на вкладці «Сповіщення» ввімкнено,
одна вкладка браузера читає вашу власну історію Ринку Steam (`steamcommunity.com/market/myhistory/`) з вашою сесією
Steam раз за обраний вами період (типово 15 хвилин) — заради найновіших продажів ваших власних лотів; нічого нікому не
надсилається. Інструменти наборів карток читають у Steam
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
якщо стеження за трейдами або його сповіщення про прийняті трейди вимкнено, ці читання списку робляться для цієї
перевірки; для тривоги про такий трейд — одне читання публічного профілю Steam його партнера, а за ознаки фішингу — і
партнера скасованого трейду, щоб тривога показала нікнейм); ваш власний інвентар із сервера Steam, щоб порівняти з
тим, що показує сторінка інвентаря, — коли ви відкриваєте свій інвентар (типово не частіше ніж раз на 6 годин;
приблизно один запит на гру й категорію предметів), а в проміжках лише його загальні кількості з однієї вкладки;
(з 1.12.1) вашу власну сторінку надісланих трейдів (`steamcommunity.com/…/tradeoffers/sent/`, адреса, яку ви відкрили),
коли ви її відкриваєте або вікно надісланого вами трейду, — не частіше ніж один запит на хвилину з однієї вкладки,
відповідь використовується 5 хвилин,
— лише щоб порівняти з тим, що показує сторінка (трейд, який щось у вашому браузері ховає); (з 1.12.2) вашу власну
сторінку вхідних трейдів (`steamcommunity.com/…/tradeoffers/`) так само, коли ви відкриваєте її або вікно одного з
ваших трейдів, — лише щоб порівняти предмети, які показує кожен трейд, із власним записом Steam про нього (домальовані
чи приховані предмети); (з 1.12.10) перед тим як автоприйняття прийме подарунок, — власну сторінку цього трейду
(`steamcommunity.com/tradeoffer/<id>/`), один раз за спробу, лише щоб за власним записом Steam про цей трейд
переконатися, що ви в ньому нічого не віддаєте.
Друзі й діалоги вебчату читаються на самій сторінці чату, без запитів до серверів Steam — лише аватари схожих пар
завантажуються із серверів зображень Steam (avatars.fastly.steamstatic.com або власний хост аватарів сторінки чату), як їх завантажує й сама сторінка, без cookie й
реферера. Фонова частина звертається до публічного API
магазину Steam (`store.steampowered.com/api/appdetails`, `/api/packagedetails`) по ціни й зображення ігор і пакетів
без ваших cookie, а лише для перевірки інвентаря читає ваш власний інвентар (`steamcommunity.com/inventory/…`, нічого
іншого) з вашими cookie Steam, щоб жоден скрипт сторінки не бачив і не змінював відповіді: cookie додає сам браузер;
фонова частина їх не читає й не зберігає, не йде за переадресацією й не надсилає їх на жодну іншу адресу. Фонова
частина розширення так само читає й ваші сторінки надісланих (з 1.12.1) і вхідних (з 1.12.2) трейдів на
steamcommunity.com, а перед тим як автоприйняття прийме подарунок, — власну сторінку цього трейду
`steamcommunity.com/tradeoffer/<id>/` (з 1.12.10), один раз за спробу (лише ці адреси), тільки щоб порівняти їх з тим,
що показує сторінка; з власної сторінки трейду сторінка отримує лише запис Steam про цей трейд (номери його предметів,
ідентифікатор акаунта партнера (SteamID64), номер трейду й дні затримки трейду, які називає сторінка: те, що сторінка
вже показує), ніколи саму сторінку; для подарунка, який приймає автоприйняття, це одне читання заступає й власне
читання сторінки цього трейду; нічого не зберігається.
(З 1.12.1) Вартість інвентаря біля балансу гаманця читає ваші власні інвентарі (TF2, CS2, Dota 2, Steam; Rust, якщо
ваше джерело цін його оцінює) зі Steam власними запитами сторінки, з однієї вкладки, по кліку на Σ або, коли вибрано
«Автоматично», сама кожні 30 хвилин, ніколи під час прийому чи надсилання трейду. Зображення предметів завантажуються
із серверів зображень Steam. (З 1.21.23) Поки у вжитку валюта, відмінна від долара США (вашого гаманця чи вибрана в
«Показувати ціни у валюті»), власний курс Steam читається з Торгового майданчика спільноти: книга заявок одного
еталонного предмета (ключа TF2, інакше мішка самоцвітів, інакше кейса CS2) у доларах США й у кожній такій валюті
(`steamcommunity.com/market/itemordershistogram`, з вашою сесією Steam, як її запитує сторінка предмета на ринку), у
фоні приблизно раз на добу на весь браузер, після невдачі — щонайбільше кілька разів на добу (очікування подвоюється до
доби), а сторінка еталонного предмета на ринку — лише коли його відомий ідентифікатор не має книги заявок; доти їх
заступають щоденні курси marketdb.info (розділ 5). (З 1.21.23) Коли ввімкнено класичні сторінки ринку Steam, сторінка
ринку CS2, яку Steam відкриває за адресою групи, один раз питає Steam без ваших cookie про лоти цього предмета
(`steamcommunity.com/market/actions?q=QueryListingsForItem`) — лише щоб знайти його назву для класичної сторінки пошуку.
(З 1.21.15) Книга заявок предмета в іншій валюті, ніж валюта гаманця, — ще один запит до власної книги заявок Steam у
цій валюті, коли ви її вибираєте. Кількості предметів у шапці Steam (типово ключі, білети й мішки самоцвітів)
читаються з вашого власного інвентаря (кінцева точка інвентаря Steam, з вашою сесією Steam) щонайбільше раз на 15
хвилин однією вкладкою і коли ви відкриваєте сторінку інвентаря, а (з 1.21.23) — ще один раз приблизно через 20 секунд
після трейду, який бачить Smart Trader (кілька трейдів поспіль — одне читання; для трейду, прийнятого деінде, — один
список ваших вхідних трейдів і один запит на трейд по його предмети, щонайбільше три).

### 5. Додаткові сервіси
Усі додаткові сторонні сервіси й сайти — під однією галочкою (з 1.21.24, як і з 1.18.0 до 1.21.22; у 1.21.23 сайти для цін і картинок були без галочки й запитувалися в браузера кнопкою «Погоджуюсь», а сервіси, що отримують Steam ID, вмикала власна галочка): «Використовувати додаткові сторонні сервіси й сайти» на сторінці, що показується перед початком роботи Smart Trader, і «Дозволити додаткові сервіси й сайти» в параметрах розширення (та сама галочка).
Під нею: джерела цін (з 2026-10-09) marketdb.info, pricempire і публічні файли цін маркетплейсів (Market.CSGO та його сайти TF2, Dota 2 і Rust, Waxpeer, LOOT.FARM, Lis-Skins), Telegram-канал KEYS.LAND і (з 1.21.23) картинки Unusual-ефектів TF2 з itempedia.tf, що не отримують нічого про вас чи ваші предмети; три сайти репутації (backpack.tf, SteamTrades, CSGO-Rep), що отримують публічний SteamID64 партнера з обміну, якого ви переглядаєте; і (з 1.18.0) steamapis.com, що отримує ваш власний ключ і SteamID64 кожного інвентаря, завантаженого через нього.
Під час першого запуску галочка порожня, і «Погоджуюсь з Ліцензійною угодою та повідомленням про дані» тоді приймає лише угоду й повідомлення про дані: у браузера нічого не запитується, і жоден із цих сервісів не працює. З позначеною галочкою та сама кнопка також одним запитом просить браузер дозволити всі їхні сайти, і галочка вважається позначеною, лише коли браузер тримає кожен із них; якщо ви відхилите цей запит, вашу згоду однаково буде записано, а ці сервіси лишаться вимкненими, доки ви не позначите галочку в параметрах. Коли сторінка питає знову після оновлення, галочка позначена так, як ви її лишили, поки браузер ще дозволяє кожен із цих сайтів або коли браузер не може цього сказати (тоді «Погоджуюсь» із галочкою, залишеною як є, зберігає ваші сервіси такими, якими вони були: нічого не запитується, не вимикається й не повертається); коли котрийсь із цих сайтів уже не дозволено, галочка порожня, а рядок під нею каже, що раніше ви її позначили, — позначте її знову, і та сама кнопка попросить браузер дозволити їх.
Якщо її зняти — на тій сторінці, коли вона питає знову, або в параметрах, — вимикаються всі вони, а доступ до їхніх сайтів повертається браузеру; забрати дозвіл сайту можна також у власних налаштуваннях доступу до сайтів для розширення в браузері або кнопкою «Видалити всі дані Smart Trader».
Поки галочку не позначено, ціни беруться лише з Ринку Steam, без картинок Unusual-ефектів, без цін маркетплейсів, без резерву KEYS.LAND і без репутації партнерів із цих сайтів; налаштування Smart Trader на Steam показують червону табличку з кнопкою до параметрів, а його кнопка в шапці Steam блимає червоним.
Типові налаштування Smart Trader використовують ціни marketdb.info і файл цін Waxpeer (заводський Пресет 1), резерв KEYS.LAND із Telegram (коли сервер keys.land не відповідає), картинки Unusual-ефектів TF2 з itempedia.tf і сайти репутації, тож позначена галочка одразу їх запускає: репутація партнерів із backpack.tf (з його інструментами на сторінках backpack.tf), SteamTrades (з вашими cookie steamtrades.com) і CSGO-Rep.
До pricempire звертаються, лише коли ви введете власний API-ключ, до файлів цін інших маркетплейсів — лише коли ви їх виберете.
steamapis.com типово не використовується: лише коли ви виберете його джерелом великих інвентарів у налаштуваннях і збережете власний ключ на сторінці параметрів.
Списки на тій сторінці називають кожен із його сайтами, тим, що він отримує, і тим, коли до нього звертаються.
До кожного все одно звертаються, лише поки його використовує його власне налаштування Smart Trader: до джерела цін — лише поки воно вибране джерелом цін у налаштуваннях (до marketdb.info — також коли вибрано маркетплейс: його курси валют переводять ціни в доларах США, а
його списки цін оцінюють предмети, яких маркетплейс не оцінює, коли для «Предмети, яких маркетплейс не оцінює» вибрано
«marketdb.info після комісії Steam і комісії виведення»). marketdb.info — типове джерело цін Smart Trader (з 1.12.2): доки не позначено галочку (і браузер не дозволить його сайт), Smart Trader бере ціни з Ринку Steam. З 1.14.0 Smart Trader може брати ціни з кількох джерел одразу, по
черзі (пресети цін, типово ввімкнені): тоді до джерела звертаються, лише поки воно є в активному пресеті й до нього
доходить предмет — джерело вище не має ціни цього предмета (заводський Пресет 1 — KEYS.LAND → marketdb.info → Ринок
Steam → Waxpeer: файл цін Waxpeer лише для предметів CS2, Dota 2 і Rust без пропозицій на Ринку Steam і лише поки позначена галочка). З 1.21.21 вікно трейду також наперед завантажує списки цін marketdb.info інших ігор, що є
в інвентарі будь-якої сторони (налаштування «marketdb.info: завантажувати списки»; у вільний час, спершу відкриті
вкладки): той самий запит, що й вище, лише id гри та часове вікно.
Вони нічого не отримують про вас чи ваші предмети: лише гру, часове вікно чи маркетплейс цілого списку цін, а
pricempire — ще й ваш власний API-ключ. pricempire працює лише з вашим власним ключем вашого акаунта pricempire: ви
задаєте його на сторінці параметрів розширення (з 1.21.9; ключ, введений раніше в налаштуваннях Smart Trader, один раз
переноситься туди), він зберігається у власній базі даних розширення на цьому комп’ютері окремо від налаштувань, і
фонова частина розширення надсилає його лише до `api.pricempire.com` як заголовок `Authorization` його запитів, ніколи
в адресі й ніколи до іншого хоста; він ніколи не передається вебсторінкам, зокрема сторінкам Steam, і не записується в
діагностичний журнал. Сервер цін keys.land дозволений від початку (його хост встановлюється разом із розширенням),
і Smart Trader звертається до нього лише тоді, коли ці ціни увімкнені в налаштуваннях Smart Trader (KEYS.LAND →
«Використовувати ціни KEYS.LAND», з 1.12.2 увімкнено від початку; перемикач цін KEYS.LAND їх вимикає; з 1.12.4 —
єдиний перемикач цих цін із будь-яким джерелом цін, зокрема маркетплейсом), або — лише по показники обміну в Steam —
коли джерелом цін вибрано маркетплейс, а предмети, яких він не оцінює, оцінюються мінус автоматична комісія виведення,
або коли ціни Ринку Steam чи marketdb.info показуються як готівка («Готівка після комісії виведення», типово; завжди,
поки KEYS.LAND увімкнено); він нічого про вас не отримує. Telegram-канал KEYS.LAND (з 1.17.0) — резерв цих цін: він
під однією галочкою (з 1.21.24, як і з 1.18.0 до 1.21.22; у 1.21.23 — один із сайтів для цін і картинок, без галочки; у 1.17.0 мав власну галочку, не поставлену, доки ви її не ставили), а Smart Trader читає його одну публічну сторінку лише тоді, коли сервер цін keys.land не відповів,
а «Використовувати ціни KEYS.LAND» і власне налаштування (KEYS.LAND → «Коли
keys.land недоступний, брати його ціни з його публічного Telegram-каналу») увімкнені, — не частіше ніж раз на 30 хвилин (раз на хвилину, поки цін KEYS.LAND немає зовсім)
для всіх ваших вкладок разом; Telegram нічого про вас не отримує. Зняти галочку можна в параметрах будь-коли (усі вони зупиняються), дозвіл окремого сайту можна забрати у власних налаштуваннях доступу до сайтів для розширення в браузері, а кожен окремо вимикається його власним налаштуванням у Smart Trader. Жоден з них не отримує від розширення cookie, крім SteamTrades: запит до SteamTrades несе ваші власні cookie
steamtrades.com, тож сайт відповідає так, як у вашій вкладці (це потрібно, щоб пройти його перевірку на ботів); це
відбувається лише коли SteamTrades увімкнено, лише в цьому одному запиті, а токени форм його сторінки вилучаються з
відповіді, перш ніж Smart Trader її читає. Кожен з них, як і
будь-який сайт, бачить вашу IP-адресу, назву й версію браузера (User-Agent) і час запиту.

steamapis.com (з 1.18.0) — під тією самою галочкою, і типово він не використовується: він працює лише з вашим
власним API-ключем steamapis.com, який ви задаєте на сторінці параметрів розширення, і лише після того, як ви виберете
його джерелом великих інвентарів у налаштуваннях Smart Trader (типово вимкнено). Smart Trader ніколи не просить API-ключ на
сайті, у чаті чи в обміні. Ключ зберігається в сховищі розширення на цьому комп’ютері, ніколи не передається сторінкам
Steam, а фонова частина розширення надсилає його лише до `api.steamapis.com` як заголовок `x-api-key` його запитів,
ніколи в адресі й ніколи до іншого хоста. Smart Trader звертається до steamapis.com лише тоді, коли ви запускаєте
завантаження інвентаря, завеликого для власного ліміту Steam («завантажити решту» стаків чи наборів карток, «Завантажити
все» списку цін, масова дія, «Продовжити завантаження» панелі), ніколи сам; перед першим запитом він каже про вартість, а
перед тим, як через нього піде чужий інвентар, один раз питає вас про цей профіль (налаштування може дозволити лише ваш
власний або будь-який профіль). steamapis.com — незалежний платний сервіс (Datagrab OÜ, Естонія); за власною політикою
він зберігає журнали запитів із вашою IP-адресою та SteamID, які ви переглядаєте (зокрема чужими), до 2 років.

| Сервіс | Що надсилається | Коли |
| --- | --- | --- |
| Сервер цін keys.land (хост, зазначений у дозволах розширення) | лише те, яка ціна потрібна: `GET …/kl/v1/market/series?item=key` (або `ticket`, `gems`) `&range=24h`; і показники обміну ключів, квитків і самоцвітів у Steam: `GET …/kl/v1/steam/convert` (без параметрів). Нічого про вас чи ваш обліковий запис. (З 1.22.0) Списки цін CS2, які наш сервер збирає з cs2.sh (Ринок Steam і п’ять маркетплейсів: BUFF, Youpin, CSFloat, Skinport, C5Game): `GET …/v1/cs2sh/latest?sources=<джерела>` надсилає лише набір джерел; нічого про вас чи ваші предмети, ніколи назву предмета. Раз на добу також ідентифікатори предметів CS2 на маркетплейсах для посилань у картці предмета (`GET …/v1/cs2sh/ids`, без параметрів): нічого про вас. | коли показуються ціни ключів TF2, квитків чи самоцвітів (не частіше ніж раз на хвилину) — лише коли ціни KEYS.LAND увімкнені в налаштуваннях Smart Trader (з 1.12.2 увімкнено від початку; перемикач цін KEYS.LAND їх вимикає; з будь-яким джерелом цін, зокрема маркетплейсом); показники обміну — лише коли джерелом цін вибрано маркетплейс, а предмети, яких він не оцінює, оцінюються мінус автоматична комісія виведення, або коли ціни Ринку Steam чи marketdb.info показуються як готівка (типово; завжди, поки KEYS.LAND увімкнено) (не частіше ніж раз на кілька хвилин); (з 1.22.0) список цін CS2: один список, зберігається 15 хвилин, коли предмету CS2 потрібна ціна від члена cs2.sh вашого активного пресета («Ринок Steam (cs2.sh)», «Маркетплейси (cs2.sh)») або ввімкнено ціни на маркетплейсах вкладки CS2 і сторінка показує предмети CS2; файл ідентифікаторів раз на добу за тієї ж умови (зберігається 24 години); сам сервер дозволений від початку, у параметрах його можна вимкнути |
| Telegram (`t.me`), канал KEYS.LAND | лише запит публічної сторінки каналу: `GET https://t.me/s/keysland`. Нічого про вас чи ваші предмети, без cookie. Зі сторінки беруться лише ціни ключів, білетів і гемів його останнього придатного поста з цінами (попереднього на сторінці, коли новіші не вдалося прочитати або їхні ціни далекі від останніх відомих) і час поста. | лише коли позначено галочку додаткових сторонніх сервісів і сайтів і браузер дозволяє `t.me` (з 1.21.24, як і з 1.18.0 до 1.21.22; у 1.21.23 — один дозвіл на сайти для цін і картинок, запит, коли ви погоджувалися з повідомленням про дані; у 1.17.0 — власна галочка), ціни KEYS.LAND і налаштування Telegram увімкнені, а сервер цін keys.land не відповів; не частіше ніж раз на 30 хвилин (раз на хвилину, поки цін KEYS.LAND немає зовсім) |
| backpack.tf (`backpack.tf`) | публічний SteamID64 профілю чи партнера з обміну, якого ви переглядаєте: `GET https://backpack.tf/api/IGetUsers/v3?steamid=<SteamID64>` | коли ви відкриваєте профіль, пропозицію обміну чи історію обмінів |
| SteamTrades (`www.steamtrades.com`) | той самий SteamID64: `GET https://www.steamtrades.com/user/<SteamID64>`, з вашими власними cookie steamtrades.com (з 2026-10-07; потрібно, щоб пройти його перевірку на ботів) | так само |
| CSGO-Rep (`api.csgo-rep.com`) | той самий SteamID64: `POST https://api.csgo-rep.com` з `{"id": <число>, "query": {"steam_id": "<SteamID64>"}}`; час від часу `GET https://api.csgo-rep.com/config` (нічого про вас) | так само |
| marketdb.info (`marketdb.info`) | лише ідентифікатор гри й часове вікно цілого списку цін: `GET https://marketdb.info/api/v1/prices?game=<ідентифікатор гри>&hours=<24, 168 або 720>`; раз на день курси валют: `GET https://marketdb.info/api/v1/exchange-rates` (з 1.21.23 — заміна, доки не прочитано власний курс Steam, розділ 4). Нічого про вас чи ваші предмети, ніколи назви предмета. | коли показуються ціни гри, а збережений список старший за кілька годин — лише коли сервіс увімкнено і джерелом цін вибрано marketdb.info або маркетплейс (його курси валют, а його списки цін — коли «marketdb.info після комісії Steam і комісії виведення» оцінює предмети, яких маркетплейс не оцінює); з пресетами цін (з 1.14.0) — поки він є в активному пресеті й до нього доходить предмет; його курси валют — також поки в активному пресеті є маркетплейс (ціни маркетплейса у валюті вашого гаманця) |
| pricempire (`api.pricempire.com`) | ідентифікатор гри, маркетплейс і ваш власний API-ключ: `GET https://api.pricempire.com/v4/trader/items/prices?app_id=<ідентифікатор гри>&sources=<маркетплейс>&currency=USD` (з підпискою `/v4/paid/…`) із заголовком `Authorization: Bearer <ваш ключ>`; час від часу `GET https://api.pricempire.com/v4/free/status` (або `/limits`, `/currencies`) з тим самим заголовком. Більше нічого про вас чи ваші предмети. | коли показуються ціни CS2, а збережений список старший за час оновлення — лише коли pricempire вибрано джерелом цін і сервіс увімкнено; з пресетами цін (з 1.14.0) — поки маркетплейс активного пресету оцінюється через pricempire і до нього доходить предмет |
| файли цін маркетплейсів (`market.csgo.com`, `tf2.tm`, `market.dota2.net`, `rust.tm`, `api.waxpeer.com`, `loot.farm`, `lis-skins.com`) | лише запит публічного файлу цін гри, наприклад `GET https://market.csgo.com/api/v2/prices/USD.json`, `GET https://api.waxpeer.com/v1/prices?game=csgo&minified=1`, `GET https://loot.farm/fullprice.json`, `GET https://lis-skins.com/market_export_json/csgo.json`. Нічого про вас чи ваші предмети, без ключа. | коли показуються ціни гри, а збережений список старший за дві години — лише з маркетплейсу, вибраного джерелом цін, і лише коли сервіс увімкнено; з пресетами цін (з 1.14.0) — лише з маркетплейсу активного пресету, поки до нього доходить предмет |
| steamapis.com (`api.steamapis.com`) | SteamID64, гра й контекст інвентаря, який ви завантажуєте, і де починається його наступна сторінка: `GET https://api.steamapis.com/v2/steam/users/<SteamID64>/inventory/<гра>/<контекст>?count=2000&start_assetid=<id>` із заголовком `x-api-key: <ваш ключ>`. Більше нічого про вас чи ваші предмети. | (з 1.18.0) лише коли позначено галочку додаткових сторонніх сервісів і сайтів (у 1.21.23 — галочку сервісів, що отримують Steam ID), а steamapis.com вибрано джерелом у налаштуваннях Smart Trader (типово вимкнено), коли ви запускаєте завантаження (стаки, набори карток, «Завантажити все» списку цін, масова дія, «Продовжити завантаження» панелі) інвентаря, завеликого для власного ліміту Steam; чужий інвентар — лише після вашого підтвердження для цього профілю (або завжди, якщо ви так вибрали в налаштуваннях); не більше вашої денної кількості запитів |

Результати зберігаються на вашому комп’ютері кілька годин (розділ 2); списки джерел цін — лише як назви предметів із
цінами й кількостями. Сервер цін keys.land тримає автор Smart Trader;
він лише пересилає публічні дані про ціни з KEYS.LAND — незалежного сервісу, дані якого використовуються з дозволу його
власника; з 1.22.0 він також передає списки цін CS2, які наш власний сервер збирає з cs2.sh (незалежний сервіс цін, дані якого використовуються за його умовами; ключ до нього є лише на нашому сервері, ніколи в розширенні), а розширення надсилає йому лише набір потрібних джерел, нічого про вас чи ваші предмети. Сам сервер недовго зберігає лише звичайні журнали (запитану адресу й час) і нічого про ваш акаунт. backpack.tf,
SteamTrades, CSGO-Rep, marketdb.info, pricempire, steamapis.com, маркетплейси й Telegram застосовують власні умови й політики конфіденційності,
опубліковані на їхніх сайтах.

Поки позначена галочка додаткових сервісів і браузер дозволяє backpack.tf, розширення також додає свої
інструменти на відкриті вами сторінки backpack.tf (ціни лотів у посиланнях на обмін, вартість рюкзака); інакше воно там
зовсім не працює. На цих сторінках сторінці передаються
лише ваші налаштування, стан підказок і значення самих інструментів backpack.tf; ваші збережені посилання для обміну,
партнери, записи пропозицій, результати перевірки репутації, історія покупок і діагностичний журнал — ні.

Картинки Unusual-ефектів (налаштування Smart Trader → Предмети й інвентар, типово ввімкнено з 1.21.23 і ввімкнено
один раз для кожної інсталяції під час того оновлення): лише поки позначена галочка додаткових сторонніх сервісів і сайтів (з 1.21.24; у 1.21.23 — поки браузер дозволяв сайти для цін і картинок; повідомлення про дані називає itempedia.tf з його версії 15) і ввімкнене
налаштування, браузер вантажить ці картинки з itempedia.tf
(`https://itempedia.tf/assets/particles/<номер ефекту>_94x94.png`). Як і будь-який сервер зображень, він бачить вашу
IP-адресу, браузер, час, сайт Steam як джерело переходу (referrer; за типовим правилом браузера лише його адресу, як-от
`https://steamcommunity.com/`, а не адресу сторінки) і cookie, які itempedia.tf сам записав у вашому браузері; нічого про
вас чи ваш акаунт Steam не надсилається. На сторінці Steam іншою мовою Steam показує назву ефекту
перекладеною й без номера: тоді Smart Trader один раз для кожної перекладеної назви просить у Steam англійський опис
одного предмета, що її показує (запит опису предмета з розділу 4, англійською), і зберігає цю назву з номером ефекту
серед описів предметів на вашому комп’ютері (розділ 2).

3D-перегляд предметів CS2 (налаштування Smart Trader → Предмети й інвентар, типово ввімкнено): нічого не надсилається,
доки ви не натиснете «3D View». Ваш клік відкриває вибраний вами переглядач (типово 3dview.cs2inspects.com з 1.12.8;
csmarketcap.com чи swap.gg — з меню ▾), в адресі якого лише посилання огляду предмета — те саме, що Steam показує за «Inspect
in Game…». У розширенні сторінка переглядача (3dview.cs2inspects.com) показується у власному вікні Smart Trader як
вбудована сторінка з тією самою адресою; інші переглядачі, а також юзерскрипт, відкривають окреме вікно чи вкладку. Дані
ті самі: лише посилання огляду, без cookie (вбудована сторінка завантажується без них), без реферера. Першого разу Smart Trader спершу питає (це питання можна вимкнути). З 2026 року це посилання кодує сам
предмет: тип, фарбу, сід патерну, знос (флоат), наліпки й брелоки з їхнім розташуванням і зносом, лічильник StatTrak™,
текст іменного ярлика та ідентифікатор предмета, і в ньому може бути номер акаунта власника; старіше
посилання натомість містить SteamID64 власника (або ідентифікатор лота на ринку), ідентифікатор предмета й контрольне
число. Жодних cookie, сесії Steam, токена чи трейд-посилання з ним не йде; вкладка відкривається без реферера.
Переглядач бачить вашу IP-адресу, браузер і час і може передати посилання своїм власним сервісам (наприклад, своєму
3D-рендереру); діють його власні умови й політика конфіденційності. Панель
«Подробиці» розшифровує посилання на вашому комп’ютері й нічого не надсилає.

cs2.sh (з 1.22.0; вкладка CS2 → cs2.sh, типово ввімкнено) відкривається лише за вашим кліком, як звичайне посилання: кнопка «перевірити на cs2.sh» в інвентарі (своєму чи чужому, поки показано його інвентар CS2) і у вікні трейду (поки показано вкладку CS2 інвентаря партнера) відкриває сторінку цього інвентаря на cs2.sh у новій вкладці з публічним SteamID64 акаунта в адресі (вашим, власника профілю чи партнера з трейду); «Відкрити на cs2.sh» під «View in Community Market» у меню предмета відкриває сторінку предмета там, з ринковою назвою предмета в адресі. До кліку нічого не надсилається; сам Smart Trader не робить жодного запиту до cs2.sh (списки цін CS2 з розділу 5 надходять із нашого власного сервера). Вкладка відкривається без opener і реферера, без cookie, сесії Steam чи токена; cs2.sh бачить вашу IP-адресу, браузер і час, і діють його власні умови й політика конфіденційності.

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
журналів іншого. Для кожного перегляду сторінки він позначає вид сторінки Steam і сторінки, з якої ви прийшли
(фіксовані слова, як-от «inventory», ніколи адресу), випадковий код вкладки браузера й те, як сторінку відкрито; те,
що ви робите в інструментах Smart Trader, записується фіксованими словами (яка кнопка чи налаштування), ніколи не те,
що ви ввели. Він також записує кожен ваш клік на власних сторінках Steam, лише фіксованими словами: який це був елемент
(кнопка, посилання чи галочка) і де на сторінці, вид сторінки, куди веде посилання, і хто клікнув — ви чи Smart Trader;
відповіді Steam на ваші відхилення, скасування й скарги на пропозиції обміну та на ваші продажі на ринку, зняті лоти,
купівлі й замовлення на купівлю (яка дія, статус відповіді й скільки вона тривала); і які відомі розширення чи
userscript-и, що можуть із ним конфліктувати (інші інструменти для торгівлі в Steam), знайдено на сторінці, за їхніми
фіксованими назвами. Він ніколи не записує профілі: жодних SteamID, імен, аватарів, посилань на профілі чи обмін, токенів,
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
дані й вашого прийняття Ліцензійної угоди), повертає браузеру доступ додаткових сервісів до їхніх сайтів і (з 1.21.24)
видаляє бази даних Smart Trader у власній IndexedDB сайтів Steam — більші кеші з розділу 2 (`ct-cache`), списки джерел
цін (`ct-prices`) і кеші цін інструментів продажу — на steamcommunity.com і store.steampowered.com: через відкриту
вкладку Steam або, якщо жодної не відкрито, через вкладку, яку воно ненадовго відкриває у фоні й знову закриває
(checkout.steampowered.com — лише через відкриту там вкладку). Сторінка параметрів каже, де це зроблено; сайт, на
якому завершити не вдалося, названо, і повторне натискання кнопки з відкритою сторінкою цього сайту це завершує. Після
цього, доки ви не очистите дані цих сайтів у браузері, лишаються кілька дрібних перемикачів у `localStorage` сайтів
Steam (стилі світлої теми, розмиття для стрімів, лічильник кешу інструментів продажу, вкладки налаштувань, у яких ви
залишили розгорнутим блок «Додаткові налаштування») і два cookie налаштувань Steam з розділу 2 (`bMarketOptOut`,
`birthtime`). Видалення розширення теж видаляє його власне сховище, але до сховища сайтів
Steam не дістає: щоб видалити й кеші там, спершу натисніть «Видалити всі дані Smart Trader» (або очистіть дані
steamcommunity.com і store.steampowered.com у браузері). Кеші застарівають і скорочуються самі. Галочка додаткових сторонніх сервісів і сайтів (розділ 5) нічого не
видаляє: якщо її зняти, усі вони одразу зупиняються, а доступ до їхніх сайтів повертається браузеру; те, що вони
повернули раніше, лишається в кешах, доки не застаріє або доки ви його не видалите.

### 9. Зміни
Коли змінюється те, що розширення робить з даними, ця політика оновлюється, а зміна записується нижче зі своєю датою.
Коли зміна приносить новий вид даних, нового одержувача чи нове читання з вашою сесією Steam або виправляє те, що ця
політика вам казала, дата набрання чинності вгорі змінюється, а розширення знову показує повідомлення про дані й чекає
вашої згоди, перш ніж щось робити; зміна, записана з «жодного нового виду даних, одержувача чи дозволу», лишає дату й
повідомлення, з яким ви погодилися.

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
встановлення (перемикач цін KEYS.LAND вимикає його знову), типово показує ціни Ринку Steam і marketdb.info як готівку
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
що й раніше, ніколи для ціни ринку чи балансу Steam. 2026-10-16 (1.12.10) — подарунки автоприйняття підтверджує власна сторінка кожного трейду (розділ 4): перед тим як
автоприйняття прийме подарунок, фонова частина читає власну сторінку цього трейду
(`steamcommunity.com/tradeoffer/<id>/`, той самий сайт і сесія, що й раніше) замість усієї сторінки вхідних трейдів і
передає сторінці лише запис Steam про цей трейд (номери його предметів, ідентифікатор акаунта партнера, номер трейду, дні
затримки); жодного нового виду даних, одержувача чи дозволу, нічого не зберігається. 2026-10-16 (1.12.14) — 3D-перегляд
предметів CS2 у вікні Smart Trader (розділ 5): у розширенні кнопка «3D» показує 3dview.cs2inspects.com вбудованою
сторінкою у власному вікні розширення (одне вікно, те саме й для наступного предмета) замість нової вкладки; вбудована
сторінка отримує ту саму адресу (лише посилання огляду предмета), завантажується без ваших cookie й без реферера, і
розширення нічим з нею не обмінюється. Інші переглядачі й далі відкриваються у вкладці, юзерскрипт відкриває окреме
спливне вікно, а «Де «3D» показує переглядач» у налаштуваннях повертає вкладку. Жодного нового виду даних, одержувача чи
дозволу. 2026-10-16 (1.14.0) — пресети цін (розділ 5): кілька джерел цін одразу, по черзі; до кожного додаткового
джерела й далі звертаються лише після того, як позначено його прапорець, і тоді лише поки воно є в активному пресеті й
до нього доходить предмет (джерело вище не має його ціни); Waxpeer є в заводському Пресеті 1 для предметів CS2, Dota 2
і Rust без пропозицій на Ринку Steam. Жодного нового виду даних, одержувача чи дозволу. 2026-10-16 (1.15.1) —
виправлення після звірки цієї політики з кодом, без нової поведінки: таблиця розділу 5 каже, коли до кожного джерела
цін звертаються з пресетами цін; розділ 6 повніше називає, що містить файл діагностичного журналу (також вид сторінки й код
вкладки кожного перегляду, ваші дії в інструментах і кожен клік на власних сторінках Steam фіксованими словами, відповіді
Steam на ваші дії з обмінами й на ринку та знайдені розширення чи скрипти, що конфліктують); розділ 9 каже, коли повідомлення про дані
показується знову. Ліцензійну угоду перевидано як версію 2026-10-16 (її розділ 8: сервіс цін питають лише тоді, коли
його використовують ваші налаштування цін; 3D-переглядачі — так, як вони відкриваються тепер). Оскільки ці слова
змінилися, розширення знову показує повідомлення про дані (його версія 11). 2026-10-16 (1.15.2) — skinflow.gg
прибрано з 3D-переглядачів (розділ 5): це той самий сервіс, що й 3dview.cs2inspects.com; кнопка «3D» тепер відкриває
3dview.cs2inspects.com (типово), csmarketcap.com чи swap.gg, а вибраний переглядач skinflow.gg один раз стає
3dview.cs2inspects.com. Розділ 8 Ліцензійної угоди більше його не називає. Жодного нового виду даних, одержувача чи
дозволу. 2026-10-17 (1.16.1) — історія партнерів
Захисту від фішингу та скаму (розділ 2): скільки трейдів у вас було з кожним партнером і дні першого й останнього —
лише як односторонні ключові хеші SteamID партнера з кількостями й днями (а щоб рахувати кожен трейд один раз —
ключові хеші 4 000 найновіших трейдів з їхніми днями), зібрані на вашому комп’ютері зі сторінок
історії трейдів, які ви відкриваєте, трейдів, які ви приймаєте, і прийнятих надісланих трейдів, які стеження за
трейдами вже читає (жодного нового запиту, нічого не надсилається), показані як підказка на сторінках трейдів і у
вікні трейду; «Забути історію партнерів» видаляє її. Оскільки це новий вид даних на вашому комп’ютері, дата набрання
чинності змінюється, а розширення знову показує повідомлення про дані (його версія 12). Той самий випуск додає тривогу
безпеки, коли Steam завершує вашу сесію в цьому браузері, — її помічає власна перевірка стеження за трейдами (одна
тривога на вихід; щоб сказати це один раз, зберігаються лише ключовий хеш акаунта й час): жодного нового виду даних,
одержувача чи читання. 2026-10-17 (1.17.0) — Telegram-канал KEYS.LAND як резерв цін keys.land (розділи 2 і 5): коли
сервер цін keys.land не відповідає, Smart Trader може прочитати публічну сторінку каналу `https://t.me/s/keysland` (не
частіше ніж раз на 30 хвилин, без cookie) і взяти ціни ключів, білетів і гемів з його останнього придатного поста з цінами — з
попереднього на сторінці, коли новіші не вдалося прочитати або їхні ціни далекі від останніх відомих; вони зберігаються на вашому комп’ютері (шість цін, номер і час
поста). Telegram — новий одержувач (він бачить вашу IP-адресу, браузер і час цього запиту), тож дата набрання чинності
змінюється, а розширення знову показує повідомлення про дані (його версія 13); сервіс вимкнено, доки ви не поставите
його галочку. 2026-10-17 (1.18.0) — одна галочка для всіх додаткових сторонніх сервісів і сайтів (розділ 5): «Додаткові
сторонні сервіси й сайти» замість галочки для кожного сервісу на сторінці повідомлення про дані й перемикача для
кожного в параметрах; позначена, вона дозволяє всі одразу (браузер один раз просить дозволу на всі їхні сайти), знята —
вимикає всі й повертає їхні сайти браузеру, а список під нею називає кожен із його сайтами, тим, що він отримує, і тим,
коли до нього звертаються. До кожного й далі звертаються, лише поки його використовує його власне налаштування Smart
Trader. Під цією галочкою — новий додатковий сервіс steamapis.com (розділи 2 і 5): великі інвентарі завантажуються з вашим
власним ключем steamapis.com, який задається лише на сторінці параметрів розширення й надсилається лише до
api.steamapis.com; новий одержувач SteamID64 інвентарів, які ви завантажуєте через нього, — вашого і чужих (після
вашого підтвердження для того профілю або завжди, якщо ви так вибрали в налаштуваннях); типово не використовується —
до нього звертаються лише тоді, коли ви вибрали його джерелом великих інвентарів у налаштуваннях і запускаєте таке
завантаження. Через цього нового одержувача, оскільки вибір тепер один для всіх (попередній вибір окремих сервісів не
переноситься), а Ліцензійну угоду видано як версію 2026-10-17 (її розділ 8), розширення знову показує повідомлення
про дані (його версія 14) з непозначеною галочкою. 2026-10-17 (1.19.2) — Захист від фішингу та скаму (розділ 2) —
експериментальна функція, типово вимкнена: ніщо з його пункту в розділі 2 не читається й не зберігається, доки ви не
ввімкнете його вкладку в налаштуваннях Smart Trader; інсталяція, яка жодного налаштування цієї вкладки не змінювала,
вимикається один раз під час оновлення, а та, що змінювала, зберігає свій вибір. Власний запобіжник автоприйняття в
перевірці предметів трейду (подарунок приймається лише після підтвердження записом Steam про цей трейд — читання
сторінки цього трейду з розділу 4) діє незалежно від перемикача вкладки. Жодного нового виду даних, одержувача чи
читання; текст політики лише каже, що типово читається менше. 2026-10-18 (1.21.2) — запобіжник автоприйняття в
перевірці предметів трейду підпорядковується вкладці Захисту від фішингу та скаму, як і всі інші її перевірки: з
вимкненою вкладкою сторінка трейду подарунка (розділ 4) не читається, і автоприйняття приймає подарунок без
підтвердження записом Steam. Жодного нового виду даних, одержувача чи читання; дата набрання чинності не змінюється.
2026-10-24 (1.21.21) — вікно трейду наперед завантажує списки цін marketdb.info інших ігор, що є в інвентарі будь-якої
сторони (розділ 5; налаштування «marketdb.info: завантажувати списки», у вільний час): той самий запит, що й раніше,
лише id гри та часове вікно; ціна за малою кількістю продажів типово остаточна й більше не передає предмет наступному
джерелу, а пороги цін звільняють наступне джерело від предмета, про який уже відомо, що він дешевий. Жодного нового
виду даних, одержувача чи дозволу; дата набрання чинності не змінюється. 2026-10-24 (1.21.23) — картинки
Unusual-ефектів з itempedia.tf (розділ 5) типово ввімкнені, а в розширенні — серед сайтів для цін і картинок (повідомлення про дані називає itempedia.tf серед них): в адресі картинки лише номер ефекту, як і раніше; на
сторінці Steam іншою мовою англійську назву ефекту один раз для кожної перекладеної назви запитують у Steam (запит
опису предмета з розділу 4) і зберігають з описами предметів (розділ 2). Під час цього оновлення налаштування
вмикається один раз для кожної інсталяції (ваша пізніша зміна зберігається). У тій самій версії згода в розширенні стала одним кроком (розділ 5): сайти для цін і картинок, що не отримують нічого
про вас (marketdb.info, pricempire, файли цін маркетплейсів, Telegram-канал KEYS.LAND, itempedia.tf), більше не мають
галочки — їхні сайти браузер запитує, коли ви натискаєте «Погоджуюсь з Ліцензійною угодою та повідомленням про дані»
(одним запитом; якщо його відхилити, вони вимкнені, доки ви не дозволите їх у параметрах); єдина галочка, що лишилася,
— для сервісів, що отримують Steam ID (backpack.tf, SteamTrades, CSGO-Rep, steamapis.com): не позначена під час першого
запуску й позначена так, як ви її лишили, коли повідомлення показується знову; згоду на автоматичне прийняття
подарункових трейдів питають, коли ви його вмикаєте, а не на тій сторінці. Оскільки itempedia.tf тепер названо серед
цих сайтів, а картинки вмикаються для кожної інсталяції, дата набрання чинності змінюється, і розширення знову показує
повідомлення про дані (його версія 15); жодного нового виду даних. Ліцензійну угоду, показану разом із ним, видано як
версію 2026-10-24: її вступ, розділ 2 і розділ 8 описують цей один крок; її розділ про автоматизацію не змінився, тож
згода на автоматизацію, дана за версією 2026-10-17, зберігається. 2026-10-25 (1.21.24) — виправлення після перевірки
цієї політики за кодом 1.21.23 і плитками CS2 версії 1.21.24 та одна зміна: розділ 4 називає англійський опис класу
предмета TF2 чи CS2, який інструменти запитують у Steam на сторінці Steam мовою, іншою за англійську (з 1.21.23;
щонайбільше 200 за відвідування сторінки, зберігається разом з описами предметів), власний курс Steam, прочитаний із
книги заявок одного еталонного предмета на Торговому майданчику спільноти з вашою сесією Steam (з 1.21.23; курси
marketdb.info — лише заміна доти), одне читання без ваших cookie на сторінці ринку CS2, яку Steam відкриває за адресою
групи (з 1.21.23), книгу заявок предмета в іншій валюті, ніж валюта гаманця (з 1.21.15), і читання кількостей
предметів у шапці Steam (з 1.21.23 ще раз після трейду); розділ 2 — курси та ідентифікатори ваших надісланих трейдів,
що чекають на підтвердження, збережені для кнопки, що блимає в шапці (з 1.21.23), історію книги заявок індексу страху
й жадібності (з 1.21.18), два власні cookie налаштувань Steam, які записують два налаштування (bMarketOptOut,
birthtime), і те, що з 1.21.0 більші кеші зберігаються у власній IndexedDB сайтів Steam, до якої «Видалити всі дані
Smart Trader» до цієї версії не діставало. Зміна (розділ 8): «Видалити всі дані Smart Trader» тепер видаляє й ці бази —
через відкриту вкладку Steam або вкладку, яку воно ненадовго відкриває у фоні; після нього лишаються кілька дрібних
перемикачів у `localStorage` сайтів і два cookie, а видалення розширення, як і раніше, до сховища сайтів Steam не
дістає. Розділ 5 називає кнопку 3D її новою назвою, «3D View». Новий вигляд плиток CS2 і шкала флоату версії 1.21.24
лише показують власні дані Steam про предмет зі сторінки: жодного нового виду даних, одержувача чи читання. У тій самій версії згода в розширенні знову одна галочка (розділ 5, рішення власника від 2026-10-25): усі додаткові сторонні сервіси й сайти — і сайти для цін і картинок, і сервіси, що отримують Steam ID, — під однією галочкою «Використовувати додаткові сторонні сервіси й сайти», порожньою під час першого запуску; «Погоджуюсь з Ліцензійною угодою та повідомленням про дані» тоді приймає лише угоду й повідомлення, а з позначеною галочкою одним запитом просить браузер дозволити всі їхні сайти; коли повідомлення показується знову, галочка позначена так, як ви її лишили, поки браузер ще дозволяє кожен із них, а якщо її зняти там чи в параметрах, усі вони зупиняються, а доступ до їхніх сайтів повертається браузеру. Поки її не позначено, налаштування Smart Trader на Steam показують червону табличку, а його кнопка в шапці Steam блимає червоним. Жодного нового виду даних чи одержувача. Ліцензійну угоду, показану разом із ним, перевидано як версію 2026-10-25: її розділ 8 описує цю одну галочку; її розділ про автоматизацію не змінився, тож згода на автоматизацію, дана за версією 2026-10-17 чи 2026-10-24, зберігається. Оскільки ці
слова виправляють те, що ця політика вам казала, дата набрання чинності змінюється, а розширення знову показує
повідомлення про дані (його версія 16).
2026-10-31 (1.22.0) — нове читання з вашою сесією Steam і
виправлення того, що ця політика вам казала. Нове читання (розділ 4): поки сповіщення про продажі ввімкнено
(«Сповіщення» → «Продажі на Ринку Steam», вимкнено, доки ви їх не ввімкнете), одна вкладка браузера читає вашу власну
історію Ринку Steam з вашою сесією Steam раз за обраний вами період — заради найновіших продажів ваших власних лотів;
нічого нікому не надсилається. Розділ 2 називає, що для них зберігається: один запис для акаунта цього браузера під
його SteamID — найновіші продажі, про які ще не сповіщено (ринкова назва предмета, скільки заплатив покупець і скільки
отримали ви з id валюти, час продажу — для 12 найновіших; старіші лише як їхня кількість і загальні суми за кожною
валютою), час найновішої події вашої історії Ринку з id продажів цієї секунди та час останнього читання й останнього
сповіщення; нічого про покупця; «Видалити всі дані Smart Trader» видаляє його. Виправлення (розділ 2): записи на вашому
комп’ютері, яких ця політика раніше не називала, — трейди на утриманні, на які чекають кількості предметів у шапці
Steam (id трейд-оферу, кінець утримання, інвентарі, до яких надійдуть його предмети; щонайбільше 50, кожен до доби після
кінця утримання), з часом найновішого трейду, побаченого на ваших сторінках історії трейдів або трейд-оферів; темп
Quick accept (мілісекунди на предмет у його чистих прийняттях 20 предметів і більше, останні 10 для кожної гри, лише
числа); рядок діагностики на сторінці параметрів розширення про вашу відповідь на повідомлення про дані (її версія й
час, стан додаткових сервісів, id розширення) з лічильниками, що зберігаються лише в пам’яті браузера; і, у
`localStorage` сайтів Steam, у яких вкладках налаштувань ви залишили розгорнутим блок «Додаткові налаштування» (розділ
8: це значення лишається після «Видалити всі дані Smart Trader»). Розділ 5 каже, якою повертається галочка додаткових
сервісів, коли повідомлення показується знову: позначеною так, як ви її лишили, поки браузер ще дозволяє кожен із їхніх
сайтів або не може цього сказати, і порожньою з рядком під нею, коли котрийсь із них уже не дозволено; розділ 8
Ліцензійної угоди каже те саме (її версія 2026-10-25 лишається, тож згода на автоматизацію теж зберігається). Розділ 1
тепер точно каже, що зберігається до вашої згоди: лише службовий стан встановлення, без особистих даних. Розділи 2 і 5 також називають з 1.22.0 списки цін CS2, які наш сервер збирає з cs2.sh (Ринок Steam і п’ять маркетплейсів) і передає через уже зазначений сервер цін keys.land (надсилається лише набір джерел, нічого про вас чи ваші предмети; один список зберігається 15 хвилин), і cs2.sh серед сайтів, які відкриває лише ваш клік (SteamID64 інвентаря чи назва предмета в адресі, до кліку нічого). Жодного
нового одержувача чи дозволу; ваш вибір щодо додаткових сервісів, перемикач ретранслятора keys.land і ваша згода на
автоматизацію лишаються такими, якими були. Оскільки це нове читання з вашою сесією Steam, а ці слова виправляють те, що
ця політика вам казала, дата набрання чинності змінюється, а розширення знову показує повідомлення про дані — один раз
(його версія 17).

### 10. Контакт
ggggggdev@gmail.com

Smart Trader — незалежний проєкт. Він не пов’язаний з Valve Corporation, не схвалений і не спонсорований нею. Steam і
логотип Steam — товарні знаки та/або зареєстровані товарні знаки Valve Corporation у США та/або інших країнах.

---

## Русский

**Действует с:** 2026-10-31 · **Контакт:** ggggggdev@gmail.com

Smart Trader добавляет инструменты для обмена на страницы Steam: сводки предложений обмена и цены предметов, более
быстрое принятие выбранных вами предложений, помощники для инвентаря и торговой площадки, итоги истории обменов,
проверку репутации партнёров, предупреждения о фишинге и скаме и уведомления на рабочем столе. Эта политика
описывает все данные, с которыми работает расширение, куда они уходят и как их удалить. Она соответствует коду
расширения; если код начнёт иначе обращаться с данными, изменятся и эта политика, и уведомление в расширении, а
расширение снова попросит вашего согласия, прежде чем что-либо делать.

### 1. Ничего не происходит без вашего согласия
После установки расширение показывает уведомление о данных. Пока вы не нажмёте «Согласен», ничего не работает на
страницах Steam и запросов нет; хранится лишь служебное состояние установки (какие дополнительные сервисы включены,
счётчики диагностики), без личных данных.

### 2. Данные на вашем компьютере
Хранятся в вашем браузере на этом компьютере — в хранилище расширения (`chrome.storage.local`), а с 1.21.0 более
крупные кеши — в собственной IndexedDB сайтов Steam (см. после этого списка) — и никому не отправляются, в том числе
нам:
- ваши настройки Smart Trader и состояние его панелей и туров;
- метки предметов и заметки, которые инструменты ведут о предметах;
- сохранённые вами ссылки для обмена (они содержат токен ссылки партнёра, а после прочтения — никнейм партнёра и адрес
  его аватара) и ваша собственная ссылка (с вашим никнеймом и адресом аватара);
- итоги и кеши с открытых вами страниц: итоги истории обменов и инвентаря, описания предметов, цены торговой
  площадки, результаты проверки репутации, списки друзей, записи принятых вами предложений (с никнеймом партнёра),
  история корзины магазина; цены ключей, билетов и самоцветов, в последний раз прочитанные из Telegram-канала
  KEYS.LAND (шесть цен, номер и время поста, когда страница прочитана и почему последнее чтение не удалось, если так: не
  дольше недели);
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
- могут ли работать инструменты на страницах backpack.tf: одно «да / нет», которое код Smart Trader на страницах
  Steam копирует из настроек («Страницы backpack.tf» и переключатель игры «Team Fortress 2»), чтобы фоновая часть
  расширения загружала эти инструменты на backpack.tf только пока включены оба;
- ваш API-ключ pricempire, если вы зададите его на странице параметров расширения (никогда на сайте; с 1.21.9, раньше —
  в настройках Smart Trader): хранится в собственном хранилище расширения отдельно от настроек (его собственная база
  данных, которую не может прочитать ни одна веб-страница и ни одна часть расширения, работающая на странице), никогда
  не передаётся страницам Steam, фоновая часть расширения отправляет его только в pricempire (раздел 5);
- (с 1.18.0) ваш API-ключ steamapis.com, если вы зададите его на странице параметров расширения (никогда на сайте):
  хранится в собственном хранилище расширения отдельно от настроек (его собственная база данных, которую не может прочитать ни одна веб-страница и ни одна часть расширения, работающая на странице), никогда не передаётся страницам Steam, фоновая
  часть расширения отправляет его только на steamapis.com (раздел 5); и, только в этом браузере, сколько запросов прошло
  через него (в этом месяце, сегодня) и их обычное время;
- (с 1.12.0) то, что нужно Защите от фишинга и скама (отдельная вкладка в настройках Smart Trader; с 1.19.2 —
  экспериментальная функция, по умолчанию выключена: ничто из этого пункта не читается и не хранится, пока вы не
  включите одну из её проверок; с 1.22.0 каждая проверка — свой переключатель), чтобы заметить изменение, — только как односторонние ключевые хеши (отпечатки, сделанные на этом
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
  хранит своими словами два сравнённых никнейма и SteamID собеседника. Если слежение за трейдами выключено, защита держит фоновое
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
- (с 1.21.23) собственные курсы Steam для используемых валют (вашего кошелька и выбранной в «Показывать цены в
  валюте»): каждый курс со временем чтения, рыночный идентификатор эталонного предмета, из которого он прочитан, а после
  неудачного чтения — его время и сколько неудач было подряд — ничего о вас; курс используется не больше недели,
  «Очистить кэш цен» (Общие → Инструменты) удаляет их;
- (с 1.21.23) для мигающей кнопки в шапке Steam, для каждого аккаунта под его SteamID: идентификаторы ваших
  отправленных трейдов, которые ждут подтверждения в мобильном приложении Steam или по почте (не больше 100, каждый не
  больше 15 дней), и время трейдов, отправленных из этого браузера за последний час (не больше 20); удаляются, пока
  настройка этой кнопки выключена;
- (с 1.22.0) для количества предметов в шапке Steam, для каждого аккаунта под его SteamID (не больше трёх аккаунтов):
  кроме количества в каждом инвентаре и времени, когда оно прочитано, — трейды на удержании, предметов которых ждёт этот
  подсчёт (id трейд-оффера, когда Steam заканчивает удержание и в какие из ваших инвентарей — номера игры и контекста —
  придут его предметы; не больше 50, каждый до суток после конца удержания), и время самого нового трейда, увиденного
  на ваших собственных страницах истории трейдов или трейд-офферов — только количества, идентификаторы и время, без
  названий предметов;
- (с 1.22.0) темп Quick accept: сколько миллисекунд на предмет Steam потратил на чистые принятия 20 предметов и больше
  в этом браузере (последние 10 для каждой игры и для всех игр), для его обратного отсчёта и более долгих ожиданий, пока
  Steam медленный, — только числа, без трейдов и без аккаунта;
- (с 1.22.0) когда уведомления о продажах на вкладке «Уведомления» включены («Продажи на Рынке Steam», выключено, пока
  вы их не включите), одна запись для аккаунта этого браузера, под его SteamID (вход в другой аккаунт начинает её
  заново, ничего не сообщая о прежнем): самые новые продажи ваших собственных лотов на Рынке Steam, которые этот
  браузер увидел и о которых ещё не уведомил (рыночное название предмета, сколько заплатил покупатель и сколько
  получили вы с id валюты Steam, время продажи — для 12 самых новых; для более старых только их количество и общие
  суммы по каждой валюте, со временем самой давней из них), время самого нового события вашей истории Рынка
  (выставление или снятие лота, покупка, продажа) с id лотов и покупок Steam только продаж этой секунды (чтобы
  считать каждую продажу один раз) и время последнего чтения вашей истории Рынка и последнего уведомления — для одного
  уведомления за период; ничего о покупателе; когда вы выключаете уведомления, запись остаётся как есть, «Удалить все
  данные Smart Trader» удаляет её;
- (с 1.16.1) сколько трейдов у вас было с каждым торговым партнёром и дни первого и последнего из них — только как
  односторонние ключевые хеши SteamID партнёра с количествами и днями (без имён, без предметов), для каждого аккаунта
  (не больше пяти, по 2 000 партнёров), вместе с ключевыми хешами 4 000 самых новых трейдов (id трейд-оффера или
  партнёра с минутой трейда) и их днями, чтобы считать каждый трейд один раз, и тем, насколько прочитана история
  трейдов, собранные со страниц истории трейдов, которые вы открываете, трейдов, которые вы принимаете, и ваших отправленных трейдов, которые слежение за трейдами читает принятыми; Защита от фишинга и скама
  показывает «Ни одного трейда с <дата>» на трейде от партнёра, которого в ней нет. Ничего никуда не отправляется;
  «Забыть историю партнёров» (настройки Smart Trader → Защита от фишинга и скама) удаляет её;
- ваш ответ на уведомление о данных и ваше принятие Лицензионного соглашения: только его версия, время и ваш выбор
  насчёт автоматизации (автопринятия, автоотмены), без данных аккаунта; (с 1.22.0) страница параметров расширения
  (Обзор) показывает их в строке диагностики под уведомлением о данных вместе с состоянием дополнительных сервисов и id
  расширения, а также счётчики, которые хранятся только в памяти браузера, пока он не закрыт: сколько раз с запуска
  браузера показано уведомление и почему и сколько чтений хранилища расширения не удалось.

С 1.21.0 более крупные из этих записей хранятся не в хранилище расширения, а в собственной IndexedDB сайтов Steam в
вашем браузере (база данных `ct-cache` сайта steamcommunity.com, а также store.steampowered.com, когда страницы
магазина пользуются этими кешами): описания предметов (на странице Steam не на английском — вместе с английскими
описаниями из раздела 4: там не больше 20 000 классов предметов, иначе 5 000; английское описание запрашивается снова
через 30 дней), цены Торговой площадки сообщества и цены книг заявок, наборы карточек и уровни значков, предметы
отправленных вами трейдов, история партнёров, журнал времени Quick accept (идентификаторы трейдов только как короткие
коды), названия предметов, которые предлагают настройки шапки, и (с 1.21.18) история книги заявок каждой открытой
вами страницы предмета для индекса страха и жадности (время, количество лотов и заявок на покупку, спред и индекс:
строка в час за 7 дней, строка в день до этого, не больше 30 дней и 500 предметов). Ничего из этого никуда не
отправляется. «Очистить кэш предметов» (описания, наборы карточек и уровни, предлагаемые названия) и «Очистить кэш
цен» (цены и история индекса страха и жадности) в настройках Smart Trader → Общие → Инструменты, а также «Забыть
историю партнёров» их удаляют; с 1.21.24 «Удалить все данные Smart Trader» на странице параметров расширения тоже
удаляет эту базу — вместе с другими базами данных Smart Trader на сайтах Steam (раздел 8).

Несколько функций страниц также хранят небольшие значения в собственном хранилище сайта Steam в вашем браузере
(`localStorage` и IndexedDB сайтов steamcommunity.com или store.steampowered.com, например кеш цен торговой
площадки для инструментов продажи и списки цен включённых вами источников цен: названия предметов с ценами и
количествами, ничего о вас; с 1.22.0 также один список цен CS2 (Рынок Steam и пять маркетплейсов), который сервер цен keys.land передаёт с cs2.sh, хранится по умолчанию 15 минут («Список cs2.sh: спрашивать снова через» на вкладке CS2), названия предметов с ценами и количествами и ничего о вас, удаляется кнопкой «Очистить» на вкладке «Источники цен»; также идентификаторы предметов CS2 на маркетплейсах (Buff, Youpin, C5GAME) для ссылок в карточке предмета, один файл с того же сервера, хранится 24 часа, ничего о вас, удаляется той же кнопкой «Очистить»; с 1.12.1, пока включено размытие для стримов, — какое из трёх включено: кошелёк, имена,
аватары, чтобы оно действовало с первого кадра страницы; с 1.22.0 — в каких вкладках настроек вы оставили развёрнутым
блок «Дополнительные настройки»), как это делают и сами страницы Steam. С 1.21.24 «Удалить все
данные Smart Trader» удаляет и эти базы IndexedDB (раздел 8); несколько значений в `localStorage` остаются, пока вы не
очистите данные этого сайта в браузере. Две настройки также записывают по одному собственному cookie настроек Steam,
как это делают кнопки самого Steam: «Загружать классические страницы рынка Steam вместо Market Beta» (Продажа и рынок;
с 1.21.18 по умолчанию включено для новых установок) записывает `bMarketOptOut` на steamcommunity.com/market —
значение собственной кнопки Steam «Exit Market Beta», чтобы Steam отдавал классические страницы рынка там, где они ещё
есть; когда настройка выключена, расширение удаляет записанный им cookie, — а «Пропускать проверку возраста в
магазине» (Магазин Steam, по умолчанию включено) записывает `birthtime` на store.steampowered.com — постоянную дату
рождения (1 января 1980 года), которая отвечает на проверку возраста магазина. Steam читает их вместе со своими
страницами; в них нет ничего о вас, и никуда больше они не отправляются.

### 3. Ваша сессия Steam и токены
Когда вы пользуетесь страницами Steam, код расширения на странице использует идентификатор сессии и веб-токен,
которые держит сама открытая страница Steam, и токены ссылок для обмена. Они используются **только** в запросах к
Steam (`steamcommunity.com`, `store.steampowered.com`, `checkout.steampowered.com`, `api.steampowered.com`) — так же,
как их использовала бы страница Steam. Идентификатор сессии и веб-токен расширение никогда не сохраняет и не передаёт
своей фоновой части. Токены ссылок хранятся только внутри сохранённых вами ссылок (раздел 2). Ни один из них никуда
больше не отправляется: фоновая часть расширения отклоняет любой запрос к сайту не Steam, похожий на содержащий его.

### 4. Запросы к Steam
Инструменты читают открытые вами страницы Steam и запрашивают у Steam больше того же (историю, описания предметов,
цены, состояние предложений) с вашей сессией Steam, как это сделала бы страница. (С 1.21.23) На странице Steam на языке, отличном
от английского, они также запрашивают у Steam английское описание класса предмета TF2 или CS2, строки которого не
могут прочитать на этом языке (не более 200 за посещение страницы, в фоне; хранится вместе с описаниями предметов
раздела 2 и запрашивается снова через 30 дней); это уходит только в Steam. (С 1.22.0) Пока уведомления о продажах на
вкладке «Уведомления» включены, одна вкладка браузера читает вашу собственную историю Рынка Steam
(`steamcommunity.com/market/myhistory/`) с вашей сессией Steam раз за выбранный вами период (по умолчанию 15 минут) —
ради самых новых продаж ваших собственных лотов; ничего никому не отправляется. Инструменты наборов карточек читают у
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
когда эти счётчики меняются, и не чаще раза в 5 минут, пока какой-то ваш отправленный трейд ждёт; если слежение
за трейдами или его уведомление о принятых трейдах выключены, эти чтения списка делаются для этой проверки; для
тревоги о таком трейде — одно чтение публичного профиля Steam его партнёра, а по признаку фишинга — и партнёра
отменённого трейда, чтобы тревога показала никнейм); ваш собственный инвентарь с сервера Steam, чтобы сравнить с тем,
что показывает страница инвентаря, — когда вы открываете свой инвентарь (по умолчанию не чаще раза в 6 часов; примерно
один запрос на игру и категорию предметов), а в промежутках только его общие количества из одной вкладки; (с 1.12.1)
вашу собственную страницу отправленных трейдов (`steamcommunity.com/…/tradeoffers/sent/`, адрес, который вы открыли), когда
вы её открываете или окно отправленного вами трейда, — не чаще одного запроса в минуту из одной вкладки, ответ
используется 5 минут, — только чтобы
сравнить с тем, что показывает страница (трейд, который что-то в вашем браузере скрывает); (с 1.12.2) вашу
собственную страницу входящих трейдов (`steamcommunity.com/…/tradeoffers/`) так же, когда вы открываете её или окно
одного из ваших трейдов, — только чтобы сравнить предметы, которые показывает каждый трейд, с собственной записью Steam о
нём (дорисованные или скрытые предметы); (с 1.12.10) перед тем как автопринятие примет подарок, — собственную страницу
этого трейда (`steamcommunity.com/tradeoffer/<id>/`), один раз за попытку, только чтобы по собственной записи Steam об
этом трейде убедиться, что вы в нём ничего не отдаёте. Друзья и диалоги веб-чата читаются на самой странице чата, без запросов к серверам Steam — только аватары
похожих пар загружаются с серверов изображений Steam (avatars.fastly.steamstatic.com или собственный хост аватаров страницы чата), как их загружает и сама страница, без
cookie и реферера. Фоновая часть обращается к публичному API магазина
Steam (`store.steampowered.com/api/appdetails`, `/api/packagedetails`) за ценами и изображениями игр и пакетов без
ваших cookie, а только для проверки инвентаря читает ваш собственный инвентарь (`steamcommunity.com/inventory/…`,
ничего другого) с вашими cookie Steam, чтобы ни один скрипт страницы не видел и не менял ответа: cookie добавляет сам
браузер; фоновая часть их не читает и не хранит, не следует переадресации и не отправляет их ни на какой другой адрес.
Фоновая часть расширения так же читает и ваши страницы отправленных (с 1.12.1) и входящих (с 1.12.2) трейдов на
steamcommunity.com, а перед тем как автопринятие примет подарок, — собственную страницу этого трейда
`steamcommunity.com/tradeoffer/<id>/` (с 1.12.10), один раз за попытку (только эти адреса), только чтобы сравнить их с
тем, что показывает страница; из собственной страницы трейда страница получает только запись Steam об этом трейде
(номера его предметов, идентификатор аккаунта партнёра (SteamID64), номер трейда и дни задержки трейда, которые называет
страница: то, что страница уже показывает), никогда саму страницу; для подарка, который принимает автопринятие, это одно
чтение заменяет и собственное чтение страницы этого трейда; ничего не сохраняется. (С 1.12.1) Стоимость инвентаря рядом с балансом кошелька читает ваши собственные инвентари (TF2, CS2,
Dota 2, Steam; Rust, если ваш источник цен его оценивает) из Steam собственными запросами страницы, из одной вкладки,
по клику на Σ или, когда выбрано «Автоматически», сама каждые 30 минут, никогда во время приёма или отправки трейда.
Изображения предметов загружаются с серверов изображений Steam. (С 1.21.23) Пока используется валюта, отличная от
доллара США (вашего кошелька или выбранная в «Показывать цены в валюте»), собственный курс Steam читается с Торговой
площадки сообщества: книга заявок одного эталонного предмета (ключа TF2, иначе мешка самоцветов, иначе кейса CS2) в
долларах США и в каждой такой валюте (`steamcommunity.com/market/itemordershistogram`, с вашей сессией Steam, как её
запрашивает страница предмета на рынке), в фоне примерно раз в сутки на весь браузер, после неудачи — не больше
нескольких раз в сутки (ожидание удваивается до суток), а страница эталонного предмета на рынке — только когда его
известный идентификатор не имеет книги заявок; до тех пор их заменяют ежедневные курсы marketdb.info (раздел 5).
(С 1.21.23) Когда включены классические страницы рынка Steam, страница рынка CS2, которую Steam открывает по адресу
группы, один раз спрашивает Steam без ваших cookie о лотах этого предмета
(`steamcommunity.com/market/actions?q=QueryListingsForItem`) — только чтобы найти его название для классической
страницы поиска. (С 1.21.15) Книга заявок предмета в другой валюте, чем валюта кошелька, — ещё один запрос к
собственной книге заявок Steam в этой валюте, когда вы её выбираете. Количество предметов в шапке Steam (по умолчанию
ключи, билеты и мешки самоцветов) читается из вашего собственного инвентаря (конечная точка инвентаря Steam, с вашей
сессией Steam) не чаще раза в 15 минут одной вкладкой и когда вы открываете страницу инвентаря, а (с 1.21.23) — ещё
один раз примерно через 20 секунд после трейда, который видит Smart Trader (несколько трейдов подряд — одно чтение;
для трейда, принятого в другом месте, — один список ваших входящих трейдов и один запрос на трейд за его предметами,
не больше трёх).

### 5. Дополнительные сервисы
Все дополнительные сторонние сервисы и сайты — под одним флажком (с 1.21.24, как и с 1.18.0 до 1.21.22; в 1.21.23 сайты для цен и картинок были без флажка и запрашивались у браузера кнопкой «Согласен», а сервисы, получающие Steam ID, включал собственный флажок): «Использовать дополнительные сторонние сервисы и сайты» на странице, показанной перед началом работы Smart Trader, и «Разрешить дополнительные сервисы и сайты» в параметрах расширения (тот же флажок).
Под ним: источники цен (с 2026-10-09) marketdb.info, pricempire и публичные файлы цен маркетплейсов (Market.CSGO и его сайты TF2, Dota 2 и Rust, Waxpeer, LOOT.FARM, Lis-Skins), Telegram-канал KEYS.LAND и (с 1.21.23) картинки Unusual-эффектов TF2 с itempedia.tf, которые не получают ничего о вас или ваших предметах; три сайта репутации (backpack.tf, SteamTrades, CSGO-Rep), которые получают публичный SteamID64 партнёра по обмену, которого вы просматриваете; и (с 1.18.0) steamapis.com, который получает ваш собственный ключ и SteamID64 каждого инвентаря, загруженного через него.
При первом запуске флажок пустой, и «Согласен с Лицензионным соглашением и уведомлением о данных» тогда принимает только соглашение и уведомление о данных: у браузера ничего не запрашивается, и ни один из этих сервисов не работает. С отмеченным флажком та же кнопка также одним запросом просит браузер разрешить все их сайты, и флажок считается отмеченным, только когда браузер держит каждый из них; если вы отклоните этот запрос, ваше согласие всё равно будет записано, а эти сервисы останутся выключенными, пока вы не отметите флажок в параметрах. Когда страница спрашивает снова после обновления, флажок отмечен так, как вы его оставили, пока браузер ещё разрешает каждый из этих сайтов или когда браузер не может этого сказать (тогда «Согласен» с флажком, оставленным как есть, сохраняет ваши сервисы такими, какими они были: ничего не запрашивается, не выключается и не возвращается); когда какой-то из этих сайтов уже не разрешён, флажок пустой, а строка под ним говорит, что раньше вы его отметили, — отметьте его снова, и та же кнопка попросит браузер разрешить их.
Если его снять — на той странице, когда она спрашивает снова, или в параметрах, — выключаются все они, а доступ к их сайтам возвращается браузеру; забрать разрешение сайта можно также в собственных настройках доступа к сайтам для расширения в браузере или кнопкой «Удалить все данные Smart Trader».
Пока флажок не отмечен, цены берутся только с Рынка Steam, без картинок Unusual-эффектов, без цен маркетплейсов, без резерва KEYS.LAND и без репутации партнёров с этих сайтов; настройки Smart Trader на Steam показывают красную табличку с кнопкой к параметрам, а его кнопка в шапке Steam мигает красным.
Настройки Smart Trader по умолчанию используют цены marketdb.info и файл цен Waxpeer (заводской Пресет 1), резерв KEYS.LAND из Telegram (когда сервер keys.land не отвечает), картинки Unusual-эффектов TF2 с itempedia.tf и сайты репутации, поэтому отмеченный флажок сразу их запускает: репутация партнёров с backpack.tf (с его инструментами на страницах backpack.tf), SteamTrades (с вашими cookie steamtrades.com) и CSGO-Rep.
К pricempire обращаются, только когда вы введёте собственный API-ключ, к файлам цен других маркетплейсов — только когда вы их выберете.
steamapis.com по умолчанию не используется: только когда вы выберете его источником больших инвентарей в настройках и сохраните собственный ключ на странице параметров.
Списки на той странице называют каждый с его сайтами, тем, что он получает, и тем, когда к нему обращаются.
К каждому всё равно обращаются, только пока его использует его собственная настройка Smart Trader: к источнику цен — только пока он выбран источником цен в настройках (к marketdb.info — также когда выбран маркетплейс: его курсы валют переводят цены в долларах США, а его
списки цен оценивают предметы, которые маркетплейс не оценивает, когда для «Предметы, которые маркетплейс не оценивает»
выбрано «marketdb.info после комиссии Steam и комиссии вывода»). marketdb.info — источник цен Smart Trader по умолчанию (с 1.12.2): пока не отмечен флажок (и браузер не разрешит его сайт), Smart Trader берёт цены с Рынка Steam. С 1.14.0 Smart Trader может брать цены из нескольких
источников сразу, по порядку (пресеты цен, по умолчанию включены): тогда к источнику обращаются, только пока он есть в
активном пресете и до него доходит предмет — у источника выше нет цены этого предмета (заводской Пресет 1 — KEYS.LAND →
marketdb.info → Рынок Steam → Waxpeer: файл цен Waxpeer только для предметов CS2, Dota 2 и Rust без предложений на
Рынке Steam и только пока отмечен флажок). С 1.21.21 окно трейда также заранее загружает списки цен
marketdb.info других игр, которые есть в инвентаре любой стороны (настройка «marketdb.info: загружать списки»; в
свободное время, сначала открытые вкладки): тот же запрос, что и выше, только id игры и временное окно. Они
ничего не получают о вас или ваших предметах: только игру, временное окно или маркетплейс целого списка цен, а
pricempire — ещё и ваш собственный API-ключ. pricempire работает только с вашим собственным ключом вашего аккаунта
pricempire: вы задаёте его на странице параметров расширения (с 1.21.9; ключ, введённый раньше в настройках Smart
Trader, один раз переносится туда), он хранится в собственной базе данных расширения на этом компьютере отдельно от
настроек, и фоновая часть расширения отправляет его только на `api.pricempire.com` как заголовок `Authorization` его
запросов, никогда в адресе и никогда на другой хост; он никогда не передаётся веб-страницам, в том числе страницам
Steam, и не записывается в диагностический журнал. Сервер цен keys.land разрешён с самого начала (его хост устанавливается вместе с
расширением), и Smart Trader обращается к нему только тогда, когда эти цены включены в настройках Smart Trader
(KEYS.LAND → «Использовать цены KEYS.LAND», с 1.12.2 включено с самого начала; переключатель цен KEYS.LAND их
выключает; с 1.12.4 — единственный переключатель этих цен с любым источником цен, в том числе маркетплейсом), или —
только за показателями обмена в Steam — когда источником цен выбран маркетплейс, а предметы, которые он не оценивает,
оцениваются минус автоматическая комиссия вывода, или когда цены Рынка Steam или marketdb.info показываются как наличные
(«Наличные после комиссии вывода», по умолчанию; всегда, пока KEYS.LAND включён); он ничего о вас не получает.
Telegram-канал KEYS.LAND (с 1.17.0) — резерв этих цен: он под одним флажком (с 1.21.24, как и с 1.18.0 до 1.21.22; в 1.21.23 — один из сайтов для цен и картинок, без флажка; в 1.17.0 у него был свой флажок, не отмеченный, пока вы его не отмечали), а Smart Trader читает его одну публичную страницу только
тогда, когда сервер цен keys.land не ответил, а «Использовать цены KEYS.LAND» и
собственная настройка (KEYS.LAND → «Когда keys.land недоступен, брать его цены из его публичного Telegram-канала»)
включены, — не чаще раза в 30 минут (раз в минуту, пока цен KEYS.LAND нет совсем) для всех ваших вкладок вместе; Telegram ничего о вас не получает. Снять флажок можно в параметрах в любой момент (все они останавливаются), разрешение отдельного сайта можно забрать в собственных настройках доступа к сайтам для расширения в браузере, а каждый отдельно выключается его собственной настройкой в Smart Trader. Ни один из них не получает от расширения cookie, кроме SteamTrades: запрос к SteamTrades несёт ваши собственные
cookie steamtrades.com, поэтому сайт отвечает так же, как в вашей вкладке (это нужно, чтобы пройти его проверку на
ботов); это происходит только когда SteamTrades включён, только в этом одном запросе, а токены форм его страницы
удаляются из ответа, прежде чем Smart Trader его читает. Каждый из
них, как и любой сайт, видит ваш IP-адрес, название и версию браузера (User-Agent) и время запроса.

steamapis.com (с 1.18.0) — под тем же флажком, и по умолчанию он не используется: он работает только с
вашим собственным API-ключом steamapis.com, который вы задаёте на странице параметров расширения, и только после того,
как вы выберете его источником больших инвентарей в настройках Smart Trader (по умолчанию выключено). Smart Trader никогда не просит API-ключ
на сайте, в чате или в обмене. Ключ хранится в хранилище расширения на этом компьютере, никогда не передаётся страницам
Steam, а фоновая часть расширения отправляет его только на `api.steamapis.com` как заголовок `x-api-key` его запросов,
никогда в адресе и никогда на другой хост. Smart Trader обращается к steamapis.com только тогда, когда вы запускаете
загрузку инвентаря, слишком большого для собственного лимита Steam («загрузить остальное» стаков или наборов карточек,
«Загрузить всё» списка цен, массовое действие, «Продолжить загрузку» панели), никогда сам; перед первым запросом он
говорит о стоимости, а перед тем, как через него пойдёт чужой инвентарь, один раз спрашивает вас об этом профиле
(настройка может разрешить только ваш собственный или любой профиль). steamapis.com — независимый платный сервис
(Datagrab OÜ, Эстония); по собственной политике он хранит журналы запросов с вашим IP-адресом и SteamID, которые вы
просматриваете (в том числе чужими), до 2 лет.

| Сервис | Что отправляется | Когда |
| --- | --- | --- |
| Сервер цен keys.land (хост, указанный в разрешениях расширения) | только то, какая цена нужна: `GET …/kl/v1/market/series?item=key` (или `ticket`, `gems`) `&range=24h`; и показатели обмена ключей, билетов и самоцветов в Steam: `GET …/kl/v1/steam/convert` (без параметров). Ничего о вас или вашей учётной записи. (С 1.22.0) Списки цен CS2, которые наш сервер собирает с cs2.sh (Рынок Steam и пять маркетплейсов: BUFF, Youpin, CSFloat, Skinport, C5Game): `GET …/v1/cs2sh/latest?sources=<источники>` отправляет только набор источников; ничего о вас или ваших предметах, никогда название предмета. Раз в сутки также идентификаторы предметов CS2 на маркетплейсах для ссылок в карточке предмета (`GET …/v1/cs2sh/ids`, без параметров): ничего о вас. | когда показываются цены ключей TF2, билетов или самоцветов (не чаще раза в минуту) — только когда цены KEYS.LAND включены в настройках Smart Trader (с 1.12.2 включено с самого начала; переключатель цен KEYS.LAND их выключает; с любым источником цен, в том числе маркетплейсом); показатели обмена — только когда источником цен выбран маркетплейс, а предметы, которые он не оценивает, оцениваются минус автоматическая комиссия вывода, или когда цены Рынка Steam или marketdb.info показываются как наличные (по умолчанию; всегда, пока KEYS.LAND включён) (не чаще раза в несколько минут); (с 1.22.0) список цен CS2: один список, хранится 15 минут, когда предмету CS2 нужна цена от члена cs2.sh вашего активного пресета («Рынок Steam (cs2.sh)», «Маркетплейсы (cs2.sh)») или включены цены на маркетплейсах вкладки CS2 и страница показывает предметы CS2; файл идентификаторов раз в сутки при том же условии (хранится 24 часа); сам сервер разрешён с самого начала, в параметрах его можно выключить |
| Telegram (`t.me`), канал KEYS.LAND | только запрос публичной страницы канала: `GET https://t.me/s/keysland`. Ничего о вас или ваших предметах, без cookie. Со страницы берутся только цены ключей, билетов и самоцветов его последнего пригодного поста с ценами (более раннего на странице, когда более новые не удалось прочитать или их цены далеки от последних известных) и время поста. | только когда отмечен флажок дополнительных сторонних сервисов и сайтов и браузер разрешает `t.me` (с 1.21.24, как и с 1.18.0 до 1.21.22; в 1.21.23 — одно разрешение на сайты для цен и картинок, запрос, когда вы соглашались с уведомлением о данных; в 1.17.0 — собственный флажок), цены KEYS.LAND и настройка Telegram включены, а сервер цен keys.land не ответил; не чаще раза в 30 минут (раз в минуту, пока цен KEYS.LAND нет совсем) |
| backpack.tf (`backpack.tf`) | публичный SteamID64 профиля или партнёра по обмену, которого вы просматриваете: `GET https://backpack.tf/api/IGetUsers/v3?steamid=<SteamID64>` | когда вы открываете профиль, предложение обмена или историю обменов |
| SteamTrades (`www.steamtrades.com`) | тот же SteamID64: `GET https://www.steamtrades.com/user/<SteamID64>`, с вашими собственными cookie steamtrades.com (с 2026-10-07; нужно, чтобы пройти его проверку на ботов) | так же |
| CSGO-Rep (`api.csgo-rep.com`) | тот же SteamID64: `POST https://api.csgo-rep.com` с `{"id": <число>, "query": {"steam_id": "<SteamID64>"}}`; время от времени `GET https://api.csgo-rep.com/config` (ничего о вас) | так же |
| marketdb.info (`marketdb.info`) | только идентификатор игры и временное окно целого списка цен: `GET https://marketdb.info/api/v1/prices?game=<идентификатор игры>&hours=<24, 168 или 720>`; раз в день курсы валют: `GET https://marketdb.info/api/v1/exchange-rates` (с 1.21.23 — замена, пока не прочитан собственный курс Steam, раздел 4). Ничего о вас или ваших предметах, никогда названия предмета. | когда показываются цены игры, а сохранённый список старше нескольких часов — только когда сервис включён и источником цен выбран marketdb.info или маркетплейс (его курсы валют, а его списки цен — когда «marketdb.info после комиссии Steam и комиссии вывода» оценивает предметы, которые маркетплейс не оценивает); с пресетами цен (с 1.14.0) — пока он есть в активном пресете и до него доходит предмет; его курсы валют — также пока в активном пресете есть маркетплейс (цены маркетплейса в валюте вашего кошелька) |
| pricempire (`api.pricempire.com`) | идентификатор игры, маркетплейс и ваш собственный API-ключ: `GET https://api.pricempire.com/v4/trader/items/prices?app_id=<идентификатор игры>&sources=<маркетплейс>&currency=USD` (с подпиской `/v4/paid/…`) с заголовком `Authorization: Bearer <ваш ключ>`; время от времени `GET https://api.pricempire.com/v4/free/status` (или `/limits`, `/currencies`) с тем же заголовком. Больше ничего о вас или ваших предметах. | когда показываются цены CS2, а сохранённый список старше времени обновления — только когда pricempire выбран источником цен и сервис включён; с пресетами цен (с 1.14.0) — пока маркетплейс активного пресета оценивается через pricempire и до него доходит предмет |
| файлы цен маркетплейсов (`market.csgo.com`, `tf2.tm`, `market.dota2.net`, `rust.tm`, `api.waxpeer.com`, `loot.farm`, `lis-skins.com`) | только запрос публичного файла цен игры, например `GET https://market.csgo.com/api/v2/prices/USD.json`, `GET https://api.waxpeer.com/v1/prices?game=csgo&minified=1`, `GET https://loot.farm/fullprice.json`, `GET https://lis-skins.com/market_export_json/csgo.json`. Ничего о вас или ваших предметах, без ключа. | когда показываются цены игры, а сохранённый список старше двух часов — только с маркетплейса, выбранного источником цен, и только когда сервис включён; с пресетами цен (с 1.14.0) — только с маркетплейса активного пресета, пока до него доходит предмет |
| steamapis.com (`api.steamapis.com`) | SteamID64, игра и контекст инвентаря, который вы загружаете, и где начинается его следующая страница: `GET https://api.steamapis.com/v2/steam/users/<SteamID64>/inventory/<игра>/<контекст>?count=2000&start_assetid=<id>` с заголовком `x-api-key: <ваш ключ>`. Больше ничего о вас или ваших предметах. | (с 1.18.0) только когда отмечен флажок дополнительных сторонних сервисов и сайтов (в 1.21.23 — флажок сервисов, получающих Steam ID), а steamapis.com выбран источником в настройках Smart Trader (по умолчанию выключено), когда вы запускаете загрузку (стаки, наборы карточек, «Загрузить всё» списка цен, массовое действие, «Продолжить загрузку» панели) инвентаря, слишком большого для собственного лимита Steam; чужой инвентарь — только после вашего подтверждения для этого профиля (или всегда, если вы так выбрали в настройках); не больше вашего дневного числа запросов |

Результаты хранятся на вашем компьютере несколько часов (раздел 2); списки источников цен — только как названия
предметов с ценами и количествами. Сервер цен keys.land держит автор Smart Trader;
он только пересылает публичные данные о ценах с KEYS.LAND — независимого сервиса, данные которого используются с
разрешения его владельца; с 1.22.0 он также передаёт списки цен CS2, которые наш собственный сервер собирает с cs2.sh (независимый сервис цен, данные которого используются по его условиям; ключ к нему есть только на нашем сервере, никогда в расширении), а расширение отправляет ему только набор нужных источников, ничего о вас или ваших предметах. Сам сервер недолго хранит только обычные журналы (запрошенный адрес и время) и ничего о вашем
аккаунте. backpack.tf, SteamTrades, CSGO-Rep, marketdb.info, pricempire, steamapis.com, маркетплейсы и Telegram применяют собственные условия
и политики конфиденциальности, опубликованные на их сайтах.

Пока отмечен флажок дополнительных сервисов и браузер разрешает backpack.tf, расширение также добавляет свои
инструменты на открытые вами страницы backpack.tf (цены лотов в ссылках на обмен, стоимость рюкзака); иначе оно там
вовсе не работает. На этих страницах странице
передаются только ваши настройки, состояние подсказок и значения самих инструментов backpack.tf; ваши сохранённые
ссылки для обмена, партнёры, записи предложений, результаты проверки репутации, история покупок и диагностический
журнал — нет.

Картинки Unusual-эффектов (настройки Smart Trader → Предметы и инвентарь, по умолчанию включено с 1.21.23 и включено
один раз для каждой установки при том обновлении): только пока отмечен флажок дополнительных сторонних сервисов и сайтов (с 1.21.24; в 1.21.23 — пока браузер разрешал сайты для цен и картинок; уведомление о данных называет itempedia.tf с его версии 15) и включена настройка, браузер загружает эти картинки с itempedia.tf
(`https://itempedia.tf/assets/particles/<номер эффекта>_94x94.png`). Как и любой сервер изображений, он видит ваш
IP-адрес, браузер, время, сайт Steam как источник перехода (referrer; по стандартному правилу браузера только его адрес,
например `https://steamcommunity.com/`, а не адрес страницы) и cookie, которые itempedia.tf сам записал в вашем
браузере; ничего о вас или вашем аккаунте Steam не отправляется. На странице Steam на другом языке Steam показывает название
эффекта переведённым и без номера: тогда Smart Trader один раз для каждого переведённого названия запрашивает у Steam
английское описание одного предмета, который его показывает (запрос описания предмета из раздела 4, на английском), и
хранит это название с номером эффекта среди описаний предметов на вашем компьютере (раздел 2).

3D-просмотр предметов CS2 (настройки Smart Trader → Предметы и инвентарь, по умолчанию включено): ничего не
отправляется, пока вы не нажмёте «3D View». Ваш клик открывает выбранный вами просмотрщик (по умолчанию
3dview.cs2inspects.com с 1.12.8; csmarketcap.com или swap.gg — из меню ▾), в адресе которого только ссылка осмотра предмета — та же, что Steam
показывает за «Inspect in Game…». В расширении страница просмотрщика (3dview.cs2inspects.com) показывается в собственном
окне Smart Trader как встроенная страница с тем же адресом; другие просмотрщики, а также юзерскрипт, открывают отдельное
окно или вкладку. Данные те же: только ссылка осмотра, без cookie (встроенная страница загружается без них), без
реферера. В первый раз Smart Trader сначала спрашивает (этот вопрос можно выключить). С 2026 года
эта ссылка кодирует сам предмет: тип, раскраску, сид паттерна, износ (флоат), наклейки и брелоки с их расположением и
износом, счётчик StatTrak™, текст именного ярлыка и идентификатор предмета, и в ней может быть номер аккаунта
владельца; более старая ссылка вместо этого содержит SteamID64 владельца (или идентификатор лота на рынке),
идентификатор предмета и контрольное число. Никаких cookie, сессии Steam, токена или трейд-ссылки с ней не уходит;
вкладка открывается без реферера. Просмотрщик видит ваш IP-адрес, браузер и время и может передать ссылку своим
собственным сервисам (например, своему 3D-рендереру); действуют его собственные условия и политика конфиденциальности. Панель «Подробности» расшифровывает ссылку на вашем компьютере и ничего не отправляет.

cs2.sh (с 1.22.0; вкладка CS2 → cs2.sh, по умолчанию включено) открывается только по вашему клику, как обычная ссылка: кнопка «проверить на cs2.sh» в инвентаре (своём или чужом, пока показан его инвентарь CS2) и в окне трейда (пока показана вкладка CS2 инвентаря партнёра) открывает страницу этого инвентаря на cs2.sh в новой вкладке с публичным SteamID64 аккаунта в адресе (вашим, владельца профиля или партнёра по трейду); «Открыть на cs2.sh» под «View in Community Market» в меню предмета открывает страницу предмета там, с рыночным названием предмета в адресе. До клика ничего не отправляется; сам Smart Trader не делает ни одного запроса к cs2.sh (списки цен CS2 из раздела 5 приходят с нашего собственного сервера). Вкладка открывается без opener и реферера, без cookie, сессии Steam или токена; cs2.sh видит ваш IP-адрес, браузер и время, и действуют его собственные условия и политика конфиденциальности.

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
Для каждого просмотра страницы он отмечает вид страницы Steam и страницы, с которой вы пришли (фиксированные слова,
например «inventory», никогда адрес), случайный код вкладки браузера и то, как страница открыта; то, что вы делаете в
инструментах Smart Trader, записывается фиксированными словами (какая кнопка или настройка), никогда не то, что вы
ввели. Он также записывает каждый ваш клик на собственных страницах Steam, только фиксированными словами: какой это был
элемент (кнопка, ссылка или галочка) и где на странице, вид страницы, куда ведёт ссылка, и кто кликнул — вы или Smart
Trader; ответы Steam на ваши отклонения, отмены и жалобы на предложения обмена и на ваши продажи на рынке, снятые лоты,
покупки и заказы на покупку (какое действие, статус ответа и сколько он длился); и какие известные расширения или
userscript-ы, которые могут с ним конфликтовать (другие инструменты для торговли в Steam), найдены на странице, по их
фиксированным названиям. Он никогда не записывает профили: никаких SteamID, имён, аватаров, ссылок на профили или обмен, токенов,
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
данных и вашего принятия Лицензионного соглашения), возвращает браузеру доступ дополнительных сервисов к их сайтам и
(с 1.21.24) удаляет базы данных Smart Trader в собственной IndexedDB сайтов Steam — более крупные кеши из раздела 2
(`ct-cache`), списки источников цен (`ct-prices`) и кеши цен инструментов продажи — на steamcommunity.com и
store.steampowered.com: через открытую вкладку Steam или, если ни одна не открыта, через вкладку, которую оно ненадолго
открывает в фоне и снова закрывает (checkout.steampowered.com — только через открытую там вкладку). Страница
параметров говорит, где это сделано; сайт, на котором завершить не удалось, назван, и повторное нажатие кнопки с
открытой страницей этого сайта это завершает. После этого, пока вы не очистите данные этих сайтов в браузере,
остаются несколько мелких переключателей в `localStorage` сайтов Steam (стили светлой темы, размытие для стримов,
счётчик кеша инструментов продажи, вкладки настроек, в которых вы оставили развёрнутым блок «Дополнительные
настройки») и два cookie настроек Steam из раздела 2 (`bMarketOptOut`, `birthtime`). Удаление
расширения тоже удаляет его собственное хранилище, но до хранилища сайтов Steam не достаёт: чтобы удалить и кеши там,
сначала нажмите «Удалить все данные Smart Trader» (или очистите данные steamcommunity.com и store.steampowered.com в
браузере). Кеши устаревают и сокращаются сами. Флажок дополнительных сторонних сервисов и сайтов (раздел 5) ничего не
удаляет: если его снять, все они сразу останавливаются, а доступ к их сайтам возвращается браузеру; то, что они
вернули раньше, остаётся в кешах, пока не устареет или пока вы его не удалите.

### 9. Изменения
Когда меняется то, что расширение делает с данными, эта политика обновляется, а изменение записывается ниже со своей
датой. Когда изменение приносит новый вид данных, нового получателя или новое чтение с вашей сессией Steam либо
исправляет то, что эта политика вам говорила, дата вступления в силу вверху меняется, а расширение снова показывает
уведомление о данных и ждёт вашего согласия, прежде чем что-либо делать; изменение, записанное с «никакого нового вида
данных, получателя или разрешения», оставляет дату и уведомление, с которым вы согласились.

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
Trader по умолчанию (раздел 5): это обновление один раз включает KEYS.LAND для каждой установки (переключатель цен
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
же анонимный запрос, что и раньше, никогда для цены рынка или баланса Steam. 2026-10-16 (1.12.10) — подарки автопринятия подтверждает собственная страница каждого трейда (раздел 4): перед тем как
автопринятие примет подарок, фоновая часть читает собственную страницу этого трейда
(`steamcommunity.com/tradeoffer/<id>/`, тот же сайт и сессия, что и раньше) вместо всей страницы входящих трейдов и
передаёт странице только запись Steam об этом трейде (номера его предметов, идентификатор аккаунта партнёра, номер
трейда, дни задержки); никакого нового вида данных, получателя или разрешения, ничего не сохраняется. 2026-10-16
(1.12.14) — 3D-просмотр предметов CS2 в окне Smart Trader (раздел 5): в расширении кнопка «3D» показывает
3dview.cs2inspects.com встроенной страницей в собственном окне расширения (одно окно, то же и для следующего предмета)
вместо новой вкладки; встроенная страница получает тот же адрес (только ссылку осмотра предмета), загружается без ваших
cookie и без реферера, и расширение ничем с ней не обменивается. Другие просмотрщики по-прежнему открываются во вкладке,
юзерскрипт открывает отдельное всплывающее окно, а «Где «3D» показывает просмотрщик» в настройках возвращает вкладку.
Никакого нового вида данных, получателя или разрешения. 2026-10-16 (1.14.0) — пресеты цен (раздел 5): несколько
источников цен сразу, по порядку; к каждому дополнительному источнику по-прежнему обращаются только после того, как
отмечен его флажок, и тогда только пока он есть в активном пресете и до него доходит предмет (у источника выше нет его
цены); Waxpeer есть в заводском Пресете 1 для предметов CS2, Dota 2 и Rust без предложений на Рынке Steam. Никакого
нового вида данных, получателя или разрешения. 2026-10-16 (1.15.1) — исправления после сверки этой политики с кодом,
без нового поведения: таблица раздела 5 говорит, когда к каждому источнику цен обращаются с пресетами цен; раздел 6
полнее называет, что содержит файл диагностического журнала (также вид страницы и код вкладки каждого просмотра, ваши
действия в инструментах и каждый клик на собственных страницах Steam фиксированными словами, ответы Steam на ваши
действия с обменами и на рынке и найденные конфликтующие расширения или скрипты); раздел 9 говорит, когда уведомление о данных показывается снова.
Лицензионное соглашение переиздано как версия 2026-10-16 (его раздел 8: сервис цен спрашивается, только когда его
используют ваши настройки цен; 3D-просмотрщики — так, как они открываются теперь). Поскольку эти слова изменились,
расширение снова показывает уведомление о данных (его версия 11). 2026-10-16 (1.15.2) — skinflow.gg убран из
3D-просмотрщиков (раздел 5): это тот же сервис, что и 3dview.cs2inspects.com; кнопка «3D» теперь открывает
3dview.cs2inspects.com (по умолчанию), csmarketcap.com или swap.gg, а выбранный просмотрщик skinflow.gg один раз
становится 3dview.cs2inspects.com. Раздел 8 Лицензионного соглашения больше его не называет. Никакого нового вида
данных, получателя или разрешения. 2026-10-17 (1.16.1) — история партнёров Защиты от
фишинга и скама (раздел 2): сколько трейдов у вас было с каждым партнёром и дни первого и последнего — только как
односторонние ключевые хеши SteamID партнёра с количествами и днями (а чтобы считать каждый трейд один раз —
ключевые хеши 4 000 самых новых трейдов с их днями), собранные на вашем компьютере со страниц истории
трейдов, которые вы открываете, трейдов, которые вы принимаете, и принятых отправленных трейдов, которые слежение за
трейдами уже читает (ни одного нового запроса, ничего не отправляется), показанные как подсказка на страницах трейдов
и в окне трейда; «Забыть историю партнёров» удаляет её. Поскольку это новый вид данных на вашем компьютере, дата
вступления в силу меняется, а расширение снова показывает уведомление о данных (его версия 12). Тот же выпуск
добавляет тревогу безопасности, когда Steam завершает вашу сессию в этом браузере, — её замечает собственная проверка
слежения за трейдами (одна тревога на выход; чтобы сказать это один раз, хранятся только ключевой хеш аккаунта и
время): никакого нового вида данных, получателя или чтения. 2026-10-17 (1.17.0) — Telegram-канал KEYS.LAND как
резерв цен keys.land (разделы 2 и 5): когда сервер цен keys.land не отвечает, Smart Trader может прочитать публичную
страницу канала `https://t.me/s/keysland` (не чаще раза в 30 минут, без cookie) и взять цены ключей, билетов и
самоцветов из его последнего пригодного поста с ценами — из более раннего на странице, когда более новые не удалось прочитать или их цены далеки от последних известных; они хранятся на
вашем компьютере (шесть цен, номер и время поста). Telegram — новый получатель (он видит ваш IP-адрес, браузер и время
этого запроса), поэтому дата вступления в силу меняется, а расширение снова показывает уведомление о данных (его версия
13); сервис выключен, пока вы не отметите его флажок. 2026-10-17 (1.18.0) — один флажок для всех дополнительных
сторонних сервисов и сайтов (раздел 5): «Сторонние сервисы и сайты» вместо флажка для каждого сервиса на
странице уведомления о данных и переключателя для каждого в параметрах; отмеченный, он разрешает все сразу (браузер
один раз просит разрешения на все их сайты), снятый — выключает все и возвращает их сайты браузеру, а список под ним
называет каждый с его сайтами, тем, что он получает, и тем, когда к нему обращаются. К каждому по-прежнему обращаются,
только пока его использует его собственная настройка Smart Trader. Под этим флажком — новый дополнительный сервис steamapis.com (разделы 2 и 5): большие инвентари загружаются с вашим
собственным ключом steamapis.com, который задаётся только на странице параметров расширения и отправляется только на
api.steamapis.com; новый получатель SteamID64 инвентарей, которые вы загружаете через него, — вашего и чужих (после
вашего подтверждения для того профиля или всегда, если вы так выбрали в настройках); по умолчанию не используется —
к нему обращаются только тогда, когда вы выбрали его источником больших инвентарей в настройках и запускаете такую
загрузку. Из-за этого нового получателя, поскольку выбор теперь один для всех (прежний выбор отдельных сервисов не
переносится), а Лицензионное соглашение выпущено как версия 2026-10-17 (его раздел 8), расширение снова показывает
уведомление о данных (его версия 14) с неотмеченным флажком. 2026-10-17 (1.19.2) — Защита от фишинга и скама
(раздел 2) — экспериментальная функция, по умолчанию выключена: ничто из её пункта в разделе 2 не читается и не
хранится, пока вы не включите её вкладку в настройках Smart Trader; установка, которая ни одной настройки этой вкладки
не меняла, выключается один раз при обновлении, а та, что меняла, сохраняет свой выбор. Собственный предохранитель
автопринятия в проверке предметов трейда (подарок принимается только после подтверждения записью Steam об этом
трейде — чтение страницы этого трейда из раздела 4) действует независимо от переключателя вкладки. Никакого нового
вида данных, получателя или чтения; текст политики лишь говорит, что по умолчанию читается меньше. 2026-10-18
(1.21.2) — предохранитель автопринятия в проверке предметов трейда подчиняется вкладке Защиты от фишинга и скама, как
и все остальные её проверки: с выключенной вкладкой страница трейда подарка (раздел 4) не читается, и автопринятие
принимает подарок без подтверждения записью Steam. Никакого нового вида данных, получателя или чтения; дата
вступления в силу не меняется. 2026-10-24 (1.21.21) — окно трейда заранее загружает списки цен marketdb.info других
игр, которые есть в инвентаре любой стороны (раздел 5; настройка «marketdb.info: загружать списки», в свободное время):
тот же запрос, что и раньше, только id игры и временное окно; цена по малому числу продаж по умолчанию окончательна и
больше не передаёт предмет следующему источнику, а пороги цен избавляют следующий источник от предмета, о котором уже
известно, что он дешёвый. Никакого нового вида данных, получателя или разрешения; дата вступления в силу не меняется.
2026-10-24 (1.21.23) — картинки Unusual-эффектов с itempedia.tf (раздел 5) по умолчанию включены, а в расширении — среди сайтов для цен и картинок (уведомление о данных называет itempedia.tf среди них): в адресе картинки
только номер эффекта, как и раньше; на странице Steam на другом языке английское название эффекта один раз для
каждого переведённого названия запрашивают у Steam (запрос описания предмета из раздела 4) и хранят с описаниями
предметов (раздел 2). При этом обновлении настройка включается один раз для каждой установки (ваше позднее
изменение сохраняется). В той же версии согласие в расширении стало одним шагом (раздел 5): сайты для цен и картинок, которые ничего не
получают о вас (marketdb.info, pricempire, файлы цен маркетплейсов, Telegram-канал KEYS.LAND, itempedia.tf), больше не
имеют флажка — их сайты браузер запрашивает, когда вы нажимаете «Согласен с Лицензионным соглашением и уведомлением о
данных» (одним запросом; если его отклонить, они выключены, пока вы не разрешите их в параметрах); единственный
оставшийся флажок — для сервисов, получающих Steam ID (backpack.tf, SteamTrades, CSGO-Rep, steamapis.com): не отмечен
при первом запуске и отмечен так, как вы его оставили, когда уведомление показывается снова; согласие на
автоматическое принятие подарочных трейдов спрашивают, когда вы его включаете, а не на той странице. Поскольку
itempedia.tf теперь назван среди этих сайтов, а картинки включаются для каждой установки, дата вступления в силу
меняется, и расширение снова показывает уведомление о данных (его версия 15); никакого нового вида данных.
Лицензионное соглашение, показанное вместе с ним, выпущено как версия 2026-10-24: его вступление, раздел 2 и раздел 8
описывают этот один шаг; его раздел об автоматизации не изменился, поэтому согласие на автоматизацию, данное по версии
2026-10-17, сохраняется. 2026-10-25 (1.21.24) — исправления после проверки этой политики по коду 1.21.23 и плиткам
CS2 версии 1.21.24 и одно изменение: раздел 4 называет английское описание класса предмета TF2 или CS2, которое
инструменты запрашивают у Steam на странице Steam на языке, отличном от английского (с 1.21.23; не более 200 за
посещение страницы, хранится вместе с описаниями предметов), собственный курс Steam, прочитанный из книги заявок
одного эталонного предмета на Торговой площадке сообщества с вашей сессией Steam (с 1.21.23; курсы marketdb.info —
лишь замена до тех пор), одно чтение без ваших cookie на странице рынка CS2, которую Steam открывает по адресу группы
(с 1.21.23), книгу заявок предмета в другой валюте, чем валюта кошелька (с 1.21.15), и чтение количества предметов в
шапке Steam (с 1.21.23 ещё раз после трейда); раздел 2 — курсы и идентификаторы ваших отправленных трейдов, ждущих
подтверждения, сохранённые для кнопки, мигающей в шапке (с 1.21.23), историю книги заявок индекса страха и жадности
(с 1.21.18), два собственных cookie настроек Steam, которые записывают две настройки (bMarketOptOut, birthtime), и
то, что с 1.21.0 более крупные кеши хранятся в собственной IndexedDB сайтов Steam, до которой «Удалить все данные
Smart Trader» до этой версии не доставало. Изменение (раздел 8): «Удалить все данные Smart Trader» теперь удаляет и
эти базы — через открытую вкладку Steam или вкладку, которую оно ненадолго открывает в фоне; после него остаются
несколько мелких переключателей в `localStorage` сайтов и два cookie, а удаление расширения, как и раньше, до
хранилища сайтов Steam не достаёт. Раздел 5 называет кнопку 3D её новым именем, «3D View». Новый вид плиток CS2 и
шкала флоата версии 1.21.24 только показывают собственные данные Steam о предмете со страницы: никакого нового вида
данных, получателя или чтения. В той же версии согласие в расширении снова один флажок (раздел 5, решение владельца от 2026-10-25): все дополнительные сторонние сервисы и сайты — и сайты для цен и картинок, и сервисы, получающие Steam ID, — под одним флажком «Использовать дополнительные сторонние сервисы и сайты», пустым при первом запуске; «Согласен с Лицензионным соглашением и уведомлением о данных» тогда принимает только соглашение и уведомление, а с отмеченным флажком одним запросом просит браузер разрешить все их сайты; когда уведомление показывается снова, флажок отмечен так, как вы его оставили, пока браузер ещё разрешает каждый из них, а если его снять там или в параметрах, все они останавливаются, а доступ к их сайтам возвращается браузеру. Пока он не отмечен, настройки Smart Trader на Steam показывают красную табличку, а его кнопка в шапке Steam мигает красным. Никакого нового вида данных или получателя. Лицензионное соглашение, показанное вместе с ним, переиздано как версия 2026-10-25: его раздел 8 описывает этот один флажок; его раздел об автоматизации не изменился, поэтому согласие на автоматизацию, данное по версии 2026-10-17 или 2026-10-24, сохраняется. Поскольку эти слова исправляют то, что эта политика вам говорила, дата вступления в
силу меняется, и расширение снова показывает уведомление о данных (его версия 16).
2026-10-31 (1.22.0) — новое чтение с вашей сессией Steam и
исправления того, что эта политика вам говорила. Новое чтение (раздел 4): пока уведомления о продажах включены
(«Уведомления» → «Продажи на Рынке Steam», выключено, пока вы их не включите), одна вкладка браузера читает вашу
собственную историю Рынка Steam с вашей сессией Steam раз за выбранный вами период — ради самых новых продаж ваших
собственных лотов; ничего никому не отправляется. Раздел 2 называет, что для них хранится: одна запись для аккаунта
этого браузера под его SteamID — самые новые продажи, о которых ещё не уведомлено (рыночное название предмета, сколько
заплатил покупатель и сколько получили вы с id валюты, время продажи — для 12 самых новых; более старые только как их
количество и общие суммы по каждой валюте), время самого нового события вашей истории Рынка с id продаж этой секунды и
время последнего чтения и последнего уведомления; ничего о покупателе; «Удалить все данные Smart Trader» удаляет её.
Исправления (раздел 2): записи на вашем компьютере, которых эта политика раньше не называла, — трейды на удержании,
которых ждёт подсчёт предметов в шапке Steam (id трейд-оффера, конец удержания, инвентари, в которые придут его
предметы; не больше 50, каждый до суток после конца удержания), со временем самого нового трейда, увиденного на ваших
страницах истории трейдов или трейд-офферов; темп Quick accept (миллисекунды на предмет в его чистых принятиях 20
предметов и больше, последние 10 для каждой игры, только числа); строка диагностики на странице параметров расширения о
вашем ответе на уведомление о данных (его версия и время, состояние дополнительных сервисов, id расширения) со
счётчиками, которые хранятся только в памяти браузера; и, в `localStorage` сайтов Steam, в каких вкладках настроек вы
оставили развёрнутым блок «Дополнительные настройки» (раздел 8: это значение остаётся после «Удалить все данные Smart
Trader»). Раздел 5 говорит, каким возвращается флажок дополнительных сервисов, когда уведомление показывается снова:
отмеченным так, как вы его оставили, пока браузер ещё разрешает каждый из их сайтов или не может этого сказать, и
пустым со строкой под ним, когда какой-то из них уже не разрешён; раздел 8 Лицензионного соглашения говорит то же самое
(его версия 2026-10-25 остаётся, поэтому согласие на автоматизацию тоже сохраняется). Раздел 1 теперь точно говорит,
что хранится до вашего согласия: только служебное состояние установки, без личных данных. Разделы 2 и 5 также называют с 1.22.0 списки цен CS2, которые наш сервер собирает с cs2.sh (Рынок Steam и пять маркетплейсов) и передаёт через уже указанный сервер цен keys.land (отправляется только набор источников, ничего о вас или ваших предметах; один список хранится 15 минут), и cs2.sh среди сайтов, которые открывает только ваш клик (SteamID64 инвентаря или название предмета в адресе, до клика ничего). Никакого нового получателя или
разрешения; ваш выбор насчёт дополнительных сервисов, переключатель ретранслятора keys.land и ваше согласие на
автоматизацию остаются такими, какими были. Поскольку это новое чтение с вашей сессией Steam, а эти слова исправляют
то, что эта политика вам говорила, дата вступления в силу меняется, и расширение снова показывает уведомление о данных —
один раз (его версия 17).

### 10. Контакт
ggggggdev@gmail.com

Smart Trader — независимый проект. Он не связан с Valve Corporation, не одобрен и не спонсируется ею. Steam и логотип
Steam — товарные знаки и/или зарегистрированные товарные знаки Valve Corporation в США и/или других странах.
