[English](README.md) · [Українська](README.uk.md) · [Русский](README.ru.md)

# Smart Trader: trading tools for Steam

Smart Trader is a free browser extension that adds trading tools to Steam's own web pages, for your own account and your own items. It sums up trade offers and the trade window, prices your items from the sources you choose, groups equal items into stacks, helps you sell on the Steam Community Market, adds details to your trade history, works with trading cards, badges and gems, has tools of its own for CS2, TF2 and Dota 2 items, and can warn you about phishing and scam attempts. Everything runs on Steam's pages with your own Steam session. Built and tested by professional traders.

### **[Install Smart Trader from the Chrome Web Store](https://chromewebstore.google.com/detail/smart-trader-trading-tool/cikfmbllbfiplfpllhbomapngmcedglo)**

For Google Chrome 116 or newer. The Chrome Web Store keeps the extension up to date. This page describes the version in the store, 1.24.0. What changed in each store version: [history of changes](CHANGELOG.en.md).

**First start.** After installation Smart Trader shows its data notice and License Agreement. Nothing runs on Steam's pages until you press "I agree to the License Agreement and the data notice". The settings open from the "Smart Trader" button in Steam's header, and every feature has its own switch there.

## Contents

- [Inventory](#inventory)
- [Selling and the Steam Market](#selling-and-the-steam-market)
- [Trade offers and trades](#trade-offers-and-trades)
- [Trade history](#trade-history)
- [Prices and price providers](#prices-and-price-providers)
- [Steam trading cards, badges, gems and booster packs](#steam-trading-cards-badges-gems-and-booster-packs)
- [CS2](#cs2)
- [TF2](#tf2)
- [Dota 2](#dota-2)
- [Security and anti-scam protections](#security-and-anti-scam-protections)
- [Notifications](#notifications)
- [Profile and store pages](#profile-and-store-pages)
- [Interface: header, navigation panel, languages, themes, tips](#interface-header-navigation-panel-languages-themes-tips)
- [Privacy and permissions](#privacy-and-permissions)
- [Languages](#languages)
- [Support](#support)

## Inventory

- **Stacks:** the box "Stacks: one tile per item, with the count" shows each item once with the number of its copies. Steam's own search, tags and pages keep working.
- **Prices beside the inventory:** a list with every item's count, unit price and total, sorted as you like, with the sums. Someone else's inventory is priced only after you press "Price this inventory".
- **Rows per inventory page:** from Steam's 5×5 up to 5×200 items on one page, loaded step by step within Steam's limits, with the wait shown.
- **Big inventories:** the whole inventory loads at Steam's pace, and clicks and page turns stay fast on tens of thousands of items. Optionally, a big inventory loads in minutes through an external inventory service with your own key (off by default; the cost is shown before the first call, and a daily cap protects your balance).
- **Select several items:** click, Ctrl + click, Shift + click or drag a box. "Select items to sell" turns on a mode where a plain click selects, with a check mark on every selected tile.
- **Trade locks on the tiles** of every game: the hold left ("⏳4d"), not tradable, or under Steam's trade protection.
- **Originality check:** a green ✓ on genuine TF2 keys, Tour of Duty Tickets, Gems and Sacks of Gems, so a look-alike from another game or a renamed item stands out. You can add items of your own.
- **Renamed items:** an "R" mark on renamed items and, if you wish, the original name everywhere ("Show the original name of renamed items everywhere").
- **Prices on all marketplaces in the item card** (off by default): a click on an item shows its prices from every source you use, with what you would receive after fees.
- The order of the stacks (Steam's order, by count, by price or by name), a reload button and the game the inventory opens on.

## Selling and the Steam Market

- **Selling buttons** in your inventory: "Sell everything", "Sell spare copies", "Sell selected", "Sell all trading cards", "Sell all cases" and "Sell on Steam's page".
- **"Review first"** shows every price, what you receive, how many of each item to sell and the sums before anything is listed. "Sell as prices come in" lists each item as soon as its price is read, after a warning.
- **Quick sell** in the item card: buttons with the lowest listing, one step under it, the highest buy order or your own price.
- **Your limits:** minimum and maximum prices per kind of item, and a warning in Steam's sell dialog when a price is far under the current lowest one.
- An item whose listing still waits for your confirmation in the Steam Mobile app or by e-mail is never listed again.
- **Within Steam's limits:** listings and removals go no faster than your delay (2 to 3 seconds by default); at about 250 listings awaiting your confirmation a sale or a relist pauses with Continue and Stop; listings that would go over Steam's wallet limit are left out. The summary at the end says why each item was left out, with a link to the setting that stopped it.
- **My listings:** search, sort, remove, "Remove all", "Relist selected", "Relist overpriced" and a price check of every listing.
- **Order book** on an item's market page: any of the market's currencies (converted by Steam), "Seller gets" after the fees for each listing, "You get" for each buy order, the step from the price before, more rows or the whole book.
- **Fear & Greed index** beside the listings of items with enough data: a gauge, a 30-day line and its six components. It is worked out on your computer and is only an indicator: nothing is bought or sold because of it.
- **Classic market pages** instead of Steam's new layout where Steam still serves them (the market's home, the search, an item's page).
- Every bulk or irreversible action asks for confirmation first.

## Trade offers and trades

- **Offer summaries:** each side's items as stacks with counts and, on a click, the market prices of both sides and the difference.
- **Big offers fold** to their biggest stacks; "Show all" brings the rest.
- **Offer value:** what you get minus what you give, "+$x" in green or "−$x" in red, with a sum over the list and a sort by profit. It is a hint only: no accept ever uses it.
- **Quick accept** for the offers you choose: a trade with a hold is never accepted, only reported, and a small list follows each accepted trade until Steam gives its result. "Quick accept all" takes the offers you selected.
- **Selected trades:** tick offers to add them up in a panel: your items and the partner's, and what you give and get in each one.
- **Load more** next to Steam's "View More" adds the next part of the list to the page, and "Decline All Active..." asks before it declines.
- **Trade window tools:** add N items, keys, metal, tickets or gems, "Take all", add by ID or the recent items, and "Quick Offer". Only the draft changes: you send the offer yourself.
- **Trade window summary** below the item picker: the tiles first (7 a row by default, foldable), then the list with prices, a copy button and your choice of order. A click on a row shows that item in the inventory above.
- **"In trade" marks** on your items that already sit in another active offer, and the add tools pass them over.
- When Steam does not allow trade-protected items and other items in one offer, a note at the tile says why, and the add tools leave such items out and say how many.
- **Partner reputation, partner history and partner check buttons:** see [Security](#security-and-anti-scam-protections). The partner check buttons are off by default: turn them on in Settings → Profiles & reputation → Reputation.
- **Auto accept of gifts** (offers in which you give nothing): off by default, and it cannot be turned on without your explicit consent to automation ("I allow automation and accept the risk"). It never accepts an offer in which you give items or one with a trade hold, and it never confirms anything in the mobile authenticator. The "AA" switch in the header turns it off at once. Steam's rules restrict automation, and you are responsible for what is accepted on your account.

## Trade history

- **Item details and pictures** in the trade history and the inventory history, the items you gave included.
- **Held trades** summed up, and a search box over the history.
- **Totals under every trade** by your price providers, and "Load Steam Market prices" for the rest.
- **Selected trades panel**, the same as on the offers pages.
- **Times in your time zone**, 12 or 24 hours, with Steam's original time in the tooltip.
- **The order of the items** in each trade (as grouped, by count, by price or by name).
- **Partner check buttons** beside each trade (off by default: Settings → Profiles & reputation → Reputation; see [Security](#security-and-anti-scam-protections)).

## Prices and price providers

- **Price presets:** several price sources at once, in order. The source higher in the list prices an item first, the next ones what it has no price of. Preset 1 is the default; you can make presets of your own, each with its own order, or use one main source.
- **KEYS.LAND cash prices** of TF2 keys, Tour of Duty Tickets and gems: on from the start and used with any preset. A switch in the settings turns them off.
- **Market prices** as the market price, as cash after the cash-out fee or as the Steam balance you would receive.
- **Show prices in:** every price, total and tooltip in your wallet's currency (the default) or in any of the market's 39 currencies, at Steam's own exchange rate.
- **Faster prices:** many items per request from the market's search; an item with few sales takes its 30-day price; while the Steam Market is limited, the next source of the preset prices the items meanwhile.
- A price from too few sales is shown in yellow. **Price floors** save requests for items already known to be cheap.
- When a source is unavailable, limited or off, every price says so: which source, since when, how old the kept prices are and when the next try is.
- **Optional sources** behind the one consent box (see [Privacy](#privacy-and-permissions)): an external price database, a price service with your own API key and the public price lists of marketplaces. API keys are entered only on the extension's options page, and web pages never see them.
- **"Compare with the Steam Market before acting"** (off by default) also reads Steam's live prices before a price check acts.
- Prices are kept in a cache all tabs share; "Clear price cache" (General → Tools) empties it.

## Steam trading cards, badges, gems and booster packs

- **Card sets:** a "Card sets" button wherever there are trading cards (your inventory, someone else's, the trade window, the offers) counts the complete sets, the leftover cards, your badge levels and the price of a set.
- **Take sets…** in the trade window puts whole sets into the offer: any number, chosen games, or only the sets you can still craft. Never half a set.
- **Craft sets…** on your badges page: first a plan with the XP and your level before and after, then badge by badge, with Stop. Nothing is crafted before you confirm the plan.
- **Level calculator** on your badges page: from your level to a dream level, the XP, the sets to craft and what they bring (emoticons, profile backgrounds, showcases, friend limit, booster pack drop rate), without any request. Its "Buy sets" menu lists independent sites that sell card sets: some of the links are partner links, and Smart Trader may get a reward for a purchase there. A site opens only on your click, and nothing is sent to it before.
- **Gems:** "Gems from selected", "Gems from spare copies" and "All items into gems". The last two ask first for the highest price of one item (US $0.05 by default), and items priced above it are left out.
- **Booster packs:** "Open all booster packs", or only the selected ones.
- Your keys, tickets and gems are counted in the header, and gems and Sacks of Gems are priced by KEYS.LAND.
- All the settings for these items are in one place: the Steam tab of the settings.

## CS2

- **CS2 tiles:** every tile takes its rarity's colour (a Doppler takes its phase's colour) with the wear, the float and the phase or pattern in its corners, in inventories and in the trade window. Two looks: vivid or contrast.
- **Float scale** of the five wear ranges under the selected item's picture and in the trade window's item hover.
- **A line with the wear, float and phase** under every listing of the classic market pages.
- **"3D View"** opens an external 3D viewer page in a Smart Trader window (or, if you choose, in a new tab), only when you click it and with only the item's inspect link. Details shows the exact float, pattern seed and phase, decoded on your computer.
- **Prices on marketplaces (cs2.sh):** the Steam Market and five marketplaces, each with its lowest listing and highest buy order, in the item card, the trade window's hover card and an item's listing page.
- **Doppler phases:** a Doppler or Gamma Doppler is priced at its own phase's price wherever the phase is known.
- **"View in cs2.sh" and "View in Pricempire"** open the item on that site in a new tab, only on your click.
- Trade-protected items carry a shield (🛡) and can still go into an offer.
- Everything about CS2 is on the CS2 tab of the settings.

## TF2

- **Item marks on the tiles:** a killstreak's tier and sheen, a glyph for each kind of spell, a crate's series, the pictures of Unusual effects and more. The TF2 tab of the settings shows every mark.
- **Full stack:** "Full stack: one stack per Steam Market listing" (on by default) stacks the items of one market name whatever their paint, spells, parts or killstreak, and a whole stack can be sold in one go.
- **Keys and metal:** add keys or metal to a trade by number, KEYS.LAND key prices, and the originality ✓ on genuine keys and tickets.
- **backpack.tf:** the partner's trust score and the extension's tools on backpack.tf pages, under the one consent box.
- Tiles read Steam's "Tradable After" line too.

## Dota 2

- **Stacks and prices** for Dota 2 items by your price preset (the Steam Market and, for items it has no listing for, a marketplace's price list).
- **Item marks on the tiles:** quality, gems, Unusual effects and styles; the Dota-2 tab of the settings explains every mark. Optionally the value of the gems inside is added to the price, and "check at steamprice.com" opens the inventory on steamprice.com in a new tab, only on your click.
- **Big inventories:** rows per page and paced loads for large Dota 2 inventories.
- **Trade locks** on the tiles, the order of the stacks and the selling tools work as for the other games.
- Dota 2 items count in the inventory value next to your wallet balance.
- Dota 2 can be the game the inventory and the trade window open on, and General → Games turns Smart Trader off for Dota 2 if you wish.

## Security and anti-scam protections

The phishing and scam protection is experimental. Every check has its own switch and is **off by default**: turn on the ones you want in the settings.

- **Security & Devices watched:** a new session or device, a changed e-mail, phone or Steam Guard raises an alert with "Yes, it was me" and a button that opens that page.
- **Offers sent from your account but not from this browser,** and the "your offer was cancelled, another one sent" pattern: an alert that warns you not to confirm anything in the mobile authenticator.
- **Hidden sent offers:** an offer Steam lists but the page hides raises an alert.
- **Items drawn by malware** on your inventory page: what the page shows is compared with Steam's own server.
- **Trade items check:** the items an offer shows are compared with Steam's record of that offer.
- **Trade windows** checked for a covered confirm button, another partner or wrong item counts, and **look-alike friends** in one-to-one web chats (group chats are never read).
- **Auto-cancel** of offers sent from your account but not from this browser: "Off" by default, and it needs your consent to automation. It cancels at most 5 offers an hour and never one you sent from this browser.
- **Partner history** on every offer and in the trade window ("7 trades · last 3 days ago"), counted on your computer and kept as one-way codes; "Forget partner history" deletes it.
- **Partner reputation** from community reputation sites (under the one consent box), and **partner check buttons** (off by default) that open the partner's page on a reputation site in a new tab when you click one.
- **"Signed out" alert** when Steam signs you out in this browser.
- Alerts come as a red banner on every open Steam page and as a desktop notification with sound. Only one-way fingerprints are kept, and nothing goes anywhere but Steam (and to your own Telegram bot, if you turn it on).
- Smart Trader does not replace Steam Guard: confirmations in the Steam Mobile app or by e-mail stay yours.

## Notifications

- **Desktop notifications** with a short sound: a new incoming offer (who sent it, what you get and give), a sent offer accepted, the results of Quick accept and auto accept, a trade that is completed or fails.
- **Sales on the Steam Market** (off by default): what sold and for how much, once per period you choose (15 minutes by default), and a big sale told at once.
- **Security alerts** and the "signed out" warning, each by its own switch.
- **Your own Telegram bot** (off by default): the notifications you tick go to a bot you make with https://t.me/Botfather; its token stays in the extension (options page).
- **The bell and the speaker** in Steam's header turn the notifications and their sound on and off in every tab.
- **"Clear all"** in Steam's notifications popup marks every Steam notification read.
- The "Incoming Offers" button blinks with the number of waiting offers.
- Every notification setting is on the Notifications tab, each with its own switch.

## Profile and store pages

- **Profiles:** copy the SteamID64, the profile link or the full info (nickname, level, SteamID64, account age) and, on your own profile, your Trade URL.
- **Reputation** on profiles, yours and others', from community reputation sites (under the one consent box).
- **Steam store:** a button to switch the store country, a game's prices in other countries, package IDs (SubID), your own links on a game or package page, the cart history (adding to the cart always asks first) and "Skip the store's age check".
- **Steam Subscriber Agreement box:** ticked by itself in the sell dialog, when you buy or place a buy order on the market and at the store checkout, once you turn it on (off by default).

## Interface: header, navigation panel, languages, themes, tips

- **Steam's header:** the "Smart Trader" button (the settings), the AA switch of auto accept, the bell and the speaker, and a phone button while an offer you sent waits for your confirmation.
- **Item counts in the header:** your keys, tickets and gems, counted again after each trade, never faster than Steam allows.
- **Inventory value** next to your wallet balance: on a click, automatically or off.
- **Navigation panel** under Steam's menu: Inventory, Trade URLs ▾ (your saved trade links), Market, the histories, Sent Offers and Incoming Offers with their counts, and your own links.
- **For streams and screen recordings:** blur the wallet balance, nicknames and logins, and avatars. A click on a blurred one shows it for a moment.
- **Settings:** tabs by area, a search over every setting, a "Changed" mark and "Reset to default" on each row, and the rarely changed rows folded under "Advanced settings".
- **Games:** a switch per game (Team Fortress 2, Counter-Strike 2, Dota 2, Steam cards, gems and booster packs, every other game). A game switched off gets nothing from Smart Trader.
- **Settings backup:** export to a file and restore from one (settings only, never keys, trade links, consents or the licence); a restore shows every change first.
- **Light theme for Steam pages** (experimental, off by default).
- **Tips and tours** only after you ask (a blinking "?" next to the auto accept switch), and a "What's new" card after each update.
- **AI tab:** "Download SKILL.md", a description of Smart Trader for an AI agent that works in your browser for you.

## Privacy and permissions

- **No analytics, no ads, no tracking.** The developer receives none of your data. The only partner links are those of the level calculator's "Buy sets" menu: they lead to independent sites and open only on your click.
- **What stays on your computer:** your settings, item marks, saved trade links, history summaries, price caches and your API keys (kept by the extension's background part, out of every web page's reach). "Delete all Smart Trader data" on the options page removes them.
- **What goes to Steam:** the requests Steam's own pages make, with your own session.
- **Key prices:** the KEYS.LAND prices and the CS2 price lists come from the author's price service. Only which price list is wanted is sent, nothing about you or your items. A switch turns the key prices off.
- **One consent box for every optional service:** "Use the optional third-party services and sites" on the first page (empty until you tick it), the same box as "Allow the optional services and sites" on the options page. Under it: the external price database marketdb.info, pricempire (with your own key), the public price lists of marketplaces, the public page of the KEYS.LAND Telegram channel (read when the key prices cannot be had otherwise), the pictures of TF2 Unusual effects, the reputation sites backpack.tf, SteamTrades and CSGO-Rep (they receive a trade partner's public SteamID64) and steamapis.com (with your own key, for big inventories). While the box is empty, none of them is asked, and prices come from the Steam Market and the author's price service. Unticking it gives their site access back to the browser. Your own Telegram bot is not under this box: it has its own switch (the Telegram card on the extension's options page).
- **Links only on your click:** the 3D viewer, cs2.sh, Pricempire and the partner check buttons open a new tab only when you click them; nothing is sent to these sites before.
- **The diagnostic log** is off by default and never leaves your computer unless you send the file yourself.
- **No remote code:** all of the extension's code is in its package.
- Full details: [PRIVACY.md](PRIVACY.md) (the privacy policy), [LICENSE-AGREEMENT.md](LICENSE-AGREEMENT.md) (the License Agreement) and [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md) (the open-source components and their licences).

## Languages

- The interface: **English, Ukrainian and Russian** (Settings → General → Language).
- Smart Trader reads Steam's item texts the same way in every Steam page language.
- Trade history dates are read in English, Ukrainian, Russian and 20 more of Steam's languages.

## Support

Questions, bug reports and ideas: **ggggggdev@gmail.com**.

For a bug report you can turn on the diagnostic log (Settings → General → Diagnostics), repeat the problem, press "Download log" and send the file. The log keeps no SteamIDs, names, page addresses or messages.

---

Smart Trader is an independent project. It is not affiliated with, endorsed or sponsored by Valve Corporation. Steam and the Steam logo are trademarks and/or registered trademarks of Valve Corporation in the U.S. and/or other countries. Other names belong to their owners.
